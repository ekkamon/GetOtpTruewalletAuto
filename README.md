# GetOtpTruewalletAuto
- Class ตัวนี้ใช้ API ของ [PushBullet](https://www.pushbullet.com/)

# Variable
- $access_token    // โทเคนที่ได้จากเว็บ PushBullet
- $iden            // เราต้อง print_r($sms->DevicesList()) ก่อนเพื่อดู Devices เเล้วทำการเเก้ไขเลข array ให้ตรง

# Example Get OTP Truemoney Wallet
```php
<?php
  require "readsms.php";
  
  $sms = new ReadSMS($access_token);
  $iden = $sms->DevicesList()["devices"][1]["iden"];
  print_r($sms->GetTrueWalletOTP($iden));
?>
```
# Result 
![Result](https://i.imgur.com/84I9oFX.jpg)
