---
UID: NF:bluetoothapis.BluetoothRegisterForAuthentication
title: BluetoothRegisterForAuthentication function
author: windows-sdk-content
description: The BluetoothRegisterForAuthentication function registers a callback function that is called when a particular Bluetooth device requests authentication.
old-location: bluetooth\bluetoothregisterforauthentication.htm
tech.root: Bluetooth
ms.assetid: f85dd076-9062-413f-863f-9d3baba322ad
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BluetoothRegisterForAuthentication, BluetoothRegisterForAuthentication function [Bluetooth], bluetooth.bluetoothregisterforauthentication, bluetoothapis/BluetoothRegisterForAuthentication
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bthprops.dll
api_name:
 - BluetoothRegisterForAuthentication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- BluetoothRegisterForAuthentication
: 
---

# BluetoothRegisterForAuthentication function


## -description


The <b>BluetoothRegisterForAuthentication</b> function registers a callback function that is called when a particular Bluetooth device requests authentication.
<div class="alert"><b>Note</b>  When developing for Windows Vista SP2 and Windows 7 the use of <a href="https://msdn.microsoft.com/en-us/library/Cc766820(v=VS.85).aspx">BluetoothRegisterForAuthenticationEx</a> is recommended.</div><div> </div>

## -parameters




### -param pbtdi

Pointer to a  <a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a> structure. The Address member is used for comparison.


### -param phRegHandle

Pointer to a structure in which the registration HANDLE is stored. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa362895(v=VS.85).aspx">BluetoothUnregisterAuthentication</a> to close the handle.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362770(v=VS.85).aspx">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362772(v=VS.85).aspx">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362776(v=VS.85).aspx">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362778(v=VS.85).aspx">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362799(v=VS.85).aspx">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362882(v=VS.85).aspx">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362883(v=VS.85).aspx">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362893(v=VS.85).aspx">BluetoothSendAuthenticationResponse</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362895(v=VS.85).aspx">BluetoothUnregisterAuthentication</a>
 

 

