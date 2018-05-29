---
UID: NF:bluetoothapis.BluetoothRegisterForAuthentication
title: BluetoothRegisterForAuthentication function
author: windows-sdk-content
description: The BluetoothRegisterForAuthentication function registers a callback function that is called when a particular Bluetooth device requests authentication.
old-location: bluetooth\bluetoothregisterforauthentication.htm
old-project: Bluetooth
ms.assetid: f85dd076-9062-413f-863f-9d3baba322ad
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: BluetoothRegisterForAuthentication, BluetoothRegisterForAuthentication function [Bluetooth], bluetooth.bluetoothregisterforauthentication, bluetoothapis/BluetoothRegisterForAuthentication
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
req.typenames: BLUETOOTH_IO_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Bthprops.dll
api_name:
-	BluetoothRegisterForAuthentication
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothRegisterForAuthentication function


## -description


The <b>BluetoothRegisterForAuthentication</b> function registers a callback function that is called when a particular Bluetooth device requests authentication.
<div class="alert"><b>Note</b>  When developing for Windows Vista SP2 and Windows 7 the use of <a href="https://msdn.microsoft.com/c9838f27-3450-4d51-be58-ce515d06d5cb">BluetoothRegisterForAuthenticationEx</a> is recommended.</div><div> </div>

## -parameters




### -param pbtdi

Pointer to a  <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure. The Address member is used for comparison.


### -param phRegHandle

Pointer to a structure in which the registration HANDLE is stored. Call the <a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a> to close the handle.


### -param pfnCallback

Function to be called when the authentication event occurs. The function should match the prototype described in PFN_AUTHENTICATION_CALLBACK.


### -param pvParam

Optional parameter to be passed through the callback function.


## -returns



Returns ERROR_SUCCESS upon successful completion, and a valid registration handle was returned in <i>phRegHandle</i>. Any other return value indicates failure.

Call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to obtain more information about the error. The following table  describes a common error:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

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



<a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a>
 

 

