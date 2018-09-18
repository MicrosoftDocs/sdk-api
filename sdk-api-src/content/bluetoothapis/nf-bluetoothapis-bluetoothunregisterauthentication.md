---
UID: NF:bluetoothapis.BluetoothUnregisterAuthentication
title: BluetoothUnregisterAuthentication function
author: windows-sdk-content
description: The BluetoothUnregisterAuthentication function removes registration for a callback routine that was previously registered with a call to the BluetoothRegisterForAuthentication function.
old-location: bluetooth\bluetoothunregisterauthentication.htm
tech.root: bluetooth
ms.assetid: bfb1a18c-e5b1-4053-8652-5a76b196bebe
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: BluetoothUnregisterAuthentication, BluetoothUnregisterAuthentication function [Bluetooth], bluetooth.bluetoothunregisterauthentication, bluetoothapis/BluetoothUnregisterAuthentication
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
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothUnregisterAuthentication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothUnregisterAuthentication function


## -description


The <b>BluetoothUnregisterAuthentication</b> function removes registration for a callback routine that was previously registered with a call to the <a href="https://msdn.microsoft.com/en-us/library/Aa362883(v=VS.85).aspx">BluetoothRegisterForAuthentication</a> function.


## -parameters




### -param hRegHandle

Handle returned by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/Aa362883(v=VS.85).aspx">BluetoothRegisterForAuthentication</a> function.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362770(v=VS.85).aspx">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362772(v=VS.85).aspx">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362776(v=VS.85).aspx">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362778(v=VS.85).aspx">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362799(v=VS.85).aspx">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362882(v=VS.85).aspx">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362883(v=VS.85).aspx">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362893(v=VS.85).aspx">BluetoothSendAuthenticationResponse</a>
 

 

