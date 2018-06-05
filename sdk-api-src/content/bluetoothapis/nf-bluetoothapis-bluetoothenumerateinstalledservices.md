---
UID: NF:bluetoothapis.BluetoothEnumerateInstalledServices
title: BluetoothEnumerateInstalledServices function
author: windows-sdk-content
description: The BluetoothEnumerateInstalledServices function enumerates the services GUIDs (Globally Unique Identifiers) enabled on a Bluetooth device.
old-location: bluetooth\bluetoothenumerateinstalledservices.htm
old-project: Bluetooth
ms.assetid: 6f32c776-3c4d-4b0f-ab81-1e880d979d3b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: BluetoothEnumerateInstalledServices, BluetoothEnumerateInstalledServices function [Bluetooth], bluetooth.bluetoothenumerateinstalledservices, bluetoothapis/BluetoothEnumerateInstalledServices
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Bthprops.dll
-	BluetoothAPIs.dll
-	Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
-	BluetoothEnumerateInstalledServices
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothEnumerateInstalledServices function


## -description


The <b>BluetoothEnumerateInstalledServices</b> function enumerates the services GUIDs (Globally Unique Identifiers) enabled on a Bluetooth device.


## -parameters




### -param hRadio

Handle of the local Bluetooth radio device. If <b>NULL</b>,   all local radios are searched for enabled services that match the radio address in <i>pbtdi</i>.


### -param pbtdi

Pointer to a <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure.


### -param pcServiceInout

TBD


### -param pGuidServices

Pointer to a buffer in memory to receive GUIDs for installed services. The buffer must be at least *<i>pcServices</i> *<b>sizeof</b>(GUID) bytes.


#### - pcServices

On input, the number of records pointed to by the <i>pGuidServices</i> parameter. On output, the number of valid records returned in the <i>pGuidServices</i> parameter. If pGuidServices is <b>NULL</b>, on output <i>pcServices</i> contains the number of services enabled.


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




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/e267df61-d0f5-434f-b49c-6899c2abfa2a">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/cb33cf35-eb1e-4953-a779-4eb38afe0c34">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/8b482d7f-56a3-47ef-be49-5272423c10f6">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/f73acbb4-119f-4a73-a338-d11e8cf7e6be">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/a17d87b2-91d7-4a03-bff7-9bc0ee48c3b4">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/530e5131-a0ab-4ddd-be73-a07f94e74f73">BluetoothGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/dd4f6468-ccc2-4072-95c5-97553308ae47">BluetoothRemoveDevice</a>
 

 

