---
UID: NF:bluetoothapis.BluetoothEnumerateInstalledServices
title: BluetoothEnumerateInstalledServices function (bluetoothapis.h)
description: The BluetoothEnumerateInstalledServices function enumerates the services GUIDs (Globally Unique Identifiers) enabled on a Bluetooth device.
helpviewer_keywords: ["BluetoothEnumerateInstalledServices","BluetoothEnumerateInstalledServices function [Bluetooth]","bluetooth.bluetoothenumerateinstalledservices","bluetoothapis/BluetoothEnumerateInstalledServices"]
old-location: bluetooth\bluetoothenumerateinstalledservices.htm
tech.root: bluetooth
ms.assetid: 6f32c776-3c4d-4b0f-ab81-1e880d979d3b
ms.date: 12/05/2018
ms.keywords: BluetoothEnumerateInstalledServices, BluetoothEnumerateInstalledServices function [Bluetooth], bluetooth.bluetoothenumerateinstalledservices, bluetoothapis/BluetoothEnumerateInstalledServices
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
req.dll: bthprops.cpl
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothEnumerateInstalledServices
 - bluetoothapis/BluetoothEnumerateInstalledServices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bthprops.cpl
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothEnumerateInstalledServices
---

# BluetoothEnumerateInstalledServices function


## -description

The <b>BluetoothEnumerateInstalledServices</b> function enumerates the services GUIDs (Globally Unique Identifiers) enabled on a Bluetooth device.

## -parameters

### -param hRadio

Handle of the local Bluetooth radio device. If <b>NULL</b>,   all local radios are searched for enabled services that match the radio address in <i>pbtdi</i>.

### -param pbtdi

Pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure.

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

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothdisplaydeviceproperties">BluetoothDisplayDeviceProperties</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfinddeviceclose">BluetoothFindDeviceClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextdevice">BluetoothFindNextDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothremovedevice">BluetoothRemoveDevice</a>