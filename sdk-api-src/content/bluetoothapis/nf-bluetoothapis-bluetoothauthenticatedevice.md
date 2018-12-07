---
UID: NF:bluetoothapis.BluetoothAuthenticateDevice
title: BluetoothAuthenticateDevice function
author: windows-sdk-content
description: Sends an authentication request to a remote Bluetooth device.
old-location: bluetooth\bluetoothauthenticatedevice.htm
tech.root: Bluetooth
ms.assetid: 9f8ff768-a794-4a61-a215-ae17e9acf620
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BluetoothAuthenticateDevice, BluetoothAuthenticateDevice function [Bluetooth], bluetooth.bluetoothauthenticatedevice, bluetoothapis/BluetoothAuthenticateDevice
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
 - BluetoothAuthenticateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothAuthenticateDevice function


## -description


The <b>BluetoothAuthenticateDevice</b> function sends an authentication request to a remote Bluetooth device.
<div class="alert"><b>Note</b>  When developing for Windows Vista SP2 and Windows 7 the use of <a href="https://msdn.microsoft.com/en-us/library/Cc766819(v=VS.85).aspx">BluetoothAuthenticateDeviceEx</a> is recommended.</div><div> </div>

## -parameters




### -param hwndParent

A window to be the parent of the Authentication wizard. If set to <b>NULL</b>, the wizard is removed from the desktop.


### -param hRadio

A valid local radio handle, or <b>NULL</b>. If <b>NULL</b>, authentication is attempted on all local radios; if any radio succeeds, the function call succeeds.


### -param pbtbi

A structure of type <a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a> that contains the record of the Bluetooth device to be authenticated.


### -param pszPasskey

A Personal Identification Number (PIN) to be used for device authentication. If set to <b>NULL</b>, the user interface is displayed and the user must follow the authentication process provided in the user interface. If <i>pszPasskey</i> is not <b>NULL</b>, no user interface is displayed. If the passkey is not  <b>NULL</b>, it must be a <b>NULL</b>-terminated string. For more information, see the Remarks section.


### -param ulPasskeyLength

The size, in characters, of <i>pszPasskey</i>. The size of <i>pszPasskey</i> must be less than or equal to <b>BLUETOOTH_MAX_PASSKEY_SIZE</b>.


## -returns



Returns <b>ERROR_SUCCESS</b> upon successful completion.

Common errors are listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The device structure in the <i>pbtdi</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The device pointed to by <i>pbtdi</i>  is already marked as authenticated.

</td>
</tr>
</table>
 




## -remarks



Some remote Bluetooth devices can only accept numeric passkeys. There is no way to identify which devices only accept numeric passkeys in advance.

The Bluetooth authentication process has two modes: Wizard mode and Transparent mode.

Wizard mode is started when <i>pszPasskey</i> is set to <b>NULL</b>, and      the Bluetooth Connection Wizard is  started. The user is prompted to enter a passkey as a step in the wizard, after which the      authentication request is sent. The user interface displays whether the authentication attempt succeeds or fails, and provides the user with an opportunity to reattempt a failed authentication.

Transparent mode is started when <i>pszPasskey</i> is not <b>NULL</b>. In Transparent mode the authentication request is sent to the remote Bluetooth device without displaying any user interface. In Transparent mode, the Bluetooth status code is mapped to a Win32 error code; the following table lists this mapping information.<table>
<tr>
<th>Bluetooth status code</th>
<th>Win32 error code</th>
</tr>
<tr>
<td>BTH_ERROR_SUCCESS</td>
<td>ERROR_SUCCESS</td>
</tr>
<tr>
<td>BTH_ERROR_NO_CONNECTION</td>
<td>ERROR_DEVICE_NOT_CONNECTED</td>
</tr>
<tr>
<td>BTH_ERROR_PAGE_TIMEOUT</td>
<td>WAIT_TIMEOUT</td>
</tr>
<tr>
<td>BTH_ERROR_HARDWARE_FAILURE</td>
<td>ERROR_GEN_FAILURE</td>
</tr>
<tr>
<td>BTH_ERROR_AUTHENTICATION_FAILURE</td>
<td>ERROR_NOT_AUTHENTICATED</td>
</tr>
<tr>
<td>BTH_ERROR_MEMORY_FULL</td>
<td>ERROR_NOT_ENOUGH_MEMORY</td>
</tr>
<tr>
<td>BTH_ERROR_CONNECTION_TIMEOUT</td>
<td>WAIT_TIMEOUT</td>
</tr>
<tr>
<td>BTH_ERROR_LMP_RESPONSE_TIMEOUT</td>
<td>WAIT_TIMEOUT</td>
</tr>
<tr>
<td>BTH_ERROR_MAX_NUMBER_OF_CONNECTIONS</td>
<td>ERROR_REQ_NOT_ACCEP</td>
</tr>
<tr>
<td>BTH_ERROR_PAIRING_NOT_ALLOWED</td>
<td>ERROR_ACCESS_DENIED</td>
</tr>
<tr>
<td>BTH_ERROR_UNSPECIFIED_ERROR</td>
<td>ERROR_NOT_READY</td>
</tr>
<tr>
<td>BTH_ERROR_LOCAL_HOST_TERMINATED_CONNECTION</td>
<td>ERROR_VC_DISCONNECTED</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc766819(v=VS.85).aspx">BluetoothAuthenticateDeviceEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362772(v=VS.85).aspx">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362776(v=VS.85).aspx">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362778(v=VS.85).aspx">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362799(v=VS.85).aspx">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362882(v=VS.85).aspx">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362883(v=VS.85).aspx">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362893(v=VS.85).aspx">BluetoothSendAuthenticationResponse</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362895(v=VS.85).aspx">BluetoothUnregisterAuthentication</a>
 

 

