---
UID: NF:bluetoothapis.BluetoothEnumerateInstalledServices
title: BluetoothEnumerateInstalledServices function
author: windows-sdk-content
description: The BluetoothEnumerateInstalledServices function enumerates the services GUIDs (Globally Unique Identifiers) enabled on a Bluetooth device.
old-location: bluetooth\bluetoothenumerateinstalledservices.htm
tech.root: Bluetooth
ms.assetid: 6f32c776-3c4d-4b0f-ab81-1e880d979d3b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BluetoothEnumerateInstalledServices, BluetoothEnumerateInstalledServices function [Bluetooth], bluetooth.bluetoothenumerateinstalledservices, bluetoothapis/BluetoothEnumerateInstalledServices
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
 - BluetoothEnumerateInstalledServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- BluetoothEnumerateInstalledServices
: 
---

# BluetoothEnumerateInstalledServices function


## -description


The <b>BluetoothEnumerateInstalledServices</b> function enumerates the services GUIDs (Globally Unique Identifiers) enabled on a Bluetooth device.


## -parameters




### -param hRadio

Handle of the local Bluetooth radio device. If <b>NULL</b>,   all local radios are searched for enabled services that match the radio address in <i>pbtdi</i>.


### -param pbtdi

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a> structure.


### -param pcServiceInout

On input, the number of records pointed to by the <i>pGuidServices</i> parameter. On output, the number of valid records returned in the <i>pGuidServices</i> parameter. If pGuidServices is <b>NULL</b>, on output <i>pcServices</i> contains the number of services enabled.


### -param pGuidServices

Pointer to a buffer in memory to receive GUIDs for installed services. The buffer must be at least *<i>pcServices</i> *<b>sizeof</b>(GUID) bytes.


## -returns



Returns ERROR_SUCCESS upon successful completion, and the pGuidServices parameter contains a complete list of enabled service GUIDs.

The following table  describes a common error:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded. The <i>pGuidServices</i> parameter contains an incomplete list of enabled service GUIDs.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362925(v=VS.85).aspx">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362774(v=VS.85).aspx">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362782(v=VS.85).aspx">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362784(v=VS.85).aspx">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362788(v=VS.85).aspx">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362795(v=VS.85).aspx">BluetoothGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362884(v=VS.85).aspx">BluetoothRemoveDevice</a>
 

 

