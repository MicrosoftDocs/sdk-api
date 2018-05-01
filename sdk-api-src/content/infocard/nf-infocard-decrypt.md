---
UID: NF:infocard.Decrypt
title: Decrypt function
author: windows-driver-content
description: Begins decryption of a fully encrypted volume, or resumes decryption of a partially encrypted volume.
old-location: security\decrypt_win32_encryptablevolume.htm
old-project: SecProv
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Decrypt, Decrypt method [Security], Decrypt method [Security], Win32_EncryptableVolume class, Win32_EncryptableVolume class [Security], Decrypt method, Win32_EncryptableVolume.Decrypt, security.decrypt_win32_encryptablevolume
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: infocard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista Enterprise, Windows Vista Ultimate [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Root\CIMV2\Security\MicrosoftVolumeEncryption
req.assembly: 
req.type-library: 
req.typenames: TEXT_SOURCE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	infocard.h
api_name:
-	Win32_EncryptableVolume.Decrypt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Decrypt function


## -description


The <b>Decrypt</b> method of the <a href="https://msdn.microsoft.com/464fa664-4330-43fa-a5e0-144d1e73cf58">Win32_EncryptableVolume</a> class begins decryption of a fully encrypted volume, or resumes decryption of a partially encrypted volume.

When decryption is paused or in-progress, this method behaves the same as <a href="https://msdn.microsoft.com/e37f3e32-5510-431e-9782-11908e65300d">ResumeConversion</a>. When encryption is paused or in-progress, this method reverts the encryption and begins decryption.

After decryption completes, all key protectors on this volume are removed from the system and the volume converts to a standard NTFS file system.
<div class="alert"><b>Note</b>  If the disc is hardware encrypted, the <b>Decrypt</b> method sets band status to "always unlocked", removes all associated metadata, and zeroes the security ID for the drive.</div><div> </div>

## -parameters




### -param hCrypto

TBD


### -param fOAEP

TBD


### -param cbInData

TBD


### -param pInData

TBD


### -param pcbOutData

TBD


### -param ppOutData

TBD




## -returns



Type: <b>uint32</b>

This method returns one of the following codes  or another error code if it fails.

This method returns immediately. If the volume is already fully decrypted and no other errors exist, this method returns 0.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FVE_E_LOCKED_VOLUME</b></dt>
<dt>2150694912 (0x80310000)</dt>
</dl>
</td>
<td width="60%">
The volume is locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FVE_E_AUTOUNLOCK_ENABLED</b></dt>
<dt>2150694953 (0x80310029)</dt>
</dl>
</td>
<td width="60%">
This volume cannot be decrypted because keys used to automatically unlock data volumes are available. 

Use <a href="https://msdn.microsoft.com/a5fef793-0634-493d-b62d-cb842844b1e8">ClearAllAutoUnlockKeys</a> to remove these keys.

</td>
</tr>
</table>
 




## -remarks



If the volume is not already fully decrypted, running <b>Decrypt</b> causes <a href="https://msdn.microsoft.com/b292a380-1b4a-4dff-948b-6494ec3b400b">GetConversionStatus</a> to indicate that decryption is progress and shows the percentage of the volume that remains encrypted.


If the protection status of the volume is "on" before this method is run, running this method changes the protection status to "off", since by definition a partially encrypted volume is not protected.

If this method is run on the currently running operating system volume and this operating system volume is being used to automatically unlock data volumes (see method <a href="https://msdn.microsoft.com/ec77b17f-545b-40a7-91b2-ff0b32b8370d">EnableAutoUnlock</a>) you must first call the method <a href="https://msdn.microsoft.com/a5fef793-0634-493d-b62d-cb842844b1e8">ClearAllAutoUnlockKeys</a>.

Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes. MOF files are not installed as part of the Windows SDK. They are installed on the server when you add the associated role by using the Server Manager. For more information about MOF files, see <a href="https://msdn.microsoft.com/26494142-2078-4d46-a794-e43973255c2d">Managed Object Format (MOF)</a>.




## -see-also




<a href="https://msdn.microsoft.com/464fa664-4330-43fa-a5e0-144d1e73cf58">Win32_EncryptableVolume</a>
 

 

