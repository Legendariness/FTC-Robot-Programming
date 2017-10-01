package org.firstinspires.ftc.teamcode;

import com.qualcomm.robotcore.eventloop.opmode.Autonomous;
import com.qualcomm.robotcore.eventloop.opmode.Disabled;
import com.qualcomm.robotcore.eventloop.opmode.LinearOpMode;
import com.qualcomm.robotcore.eventloop.opmode.TeleOp;
import com.qualcomm.robotcore.eventloop.opmode.DcMotor;
import com.qualcomm.robotcore.eventloop.opmode.ElapsedTime;

@TeleOp(name = "Forward", group = "LinearOpMode") 
public class Forward extends LinearOpMode {


private ElapsedTime runtime = newElapsedTime();

DcMotor leftMotor();
DcMotor rightMotor();

doublePower = 0.5;


public void runOpMode() throws InterruptedException {


telemetry.addData("Status", "Initialized");
telemetry.update();

rightMotor = hardwareMap.dcMotor.get("Right_Motor");
leftMotor = hardwareMap.dcMotor.get("Left_Motor");

leftMotor.setDirection(DcMotorSimple.Direction.REVERSE);

waitForStart();
runtime.reset();

leftMotor.setPower(-power);
rightMotor.setPower(power);

power = 0.0;

sleep(2000);



}

while (opModeIsActive()) {

  telemetry.addData("Status", "Run Time: " + runtime toString());
  telemetry.update();
  
  //leftMotor.setPower(-gamepad1.left_stick_y)
  //rightMotor.setPower(-gamepad1.right_stick_y)


}



}

