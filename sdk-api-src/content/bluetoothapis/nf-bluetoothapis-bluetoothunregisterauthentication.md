---
UID: NF:bluetoothapis.BluetoothUnregisterAuthentication
title: BluetoothUnregisterAuthentication function
author: windows-sdk-content
description: The BluetoothUnregisterAuthentication function removes registration for a callback routine that was previously registered with a call to the BluetoothRegisterForAuthentication function.
old-location: bluetooth\bluetoothunregisterauthentication.htm
old-project: bluetooth
ms.assetid: bfb1a18c-e5b1-4053-8652-5a76b196bebe
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BluetoothUnregisterAuthentication, BluetoothUnregisterAuthentication function [Bluetooth], bluetooth.bluetoothunregisterauthentication, bluetoothapis/BluetoothUnregisterAuthentication
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BLUETOOTH_IO_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bthprops.dll
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothUnregisterAuthentication
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothUnregisterAuthentication function


## -description


The <b>BluetoothUnregisterAuthentication</b> function removes registration for a callback routine that was previously registered with a call to the <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a> function.


## -parameters




### -param hRegHandle

Handle returned by a previous call to the <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a> function.


## -returns



Returns <b>TRUE</b> when the authentication registration is successfully removed. Returns <b>FALSE</b> if the specified handle is not successfully closed.

Call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to obtain more information about the error. The following table  describes a common error:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/9f8ff768-a794-4a61-a215-ae17e9acf620">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/81dd4925-7f0a-468f-b706-244ce99e91df">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/ca28c9cd-a271-48fa-901c-e99e063854d5">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/8f9c133e-e647-45c8-b2c6-372b18345637">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/e20ad938-cab4-4017-95bf-8d6843f048eb">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/33d34e36-dc17-4029-91bd-53ece5a93b4b">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/4483f04e-09a2-4bd4-879c-c3a263c685de">BluetoothSendAuthenticationResponse</a>
 

 

