---
UID: NF:bluetoothapis.BluetoothSetLocalServiceInfo
title: BluetoothSetLocalServiceInfo function (bluetoothapis.h)
description: Sets local service information for a specific Bluetooth radio.
helpviewer_keywords: ["BluetoothSetLocalServiceInfo","BluetoothSetLocalServiceInfo function [Bluetooth Devices]","bltooth.bluetoothsetlocalserviceinfo","bluetoothapis/BluetoothSetLocalServiceInfo","bth_funcs_036c64a4-5050-4d5d-8217-fc4ff9ef300d.xml"]
old-location: bltooth\bluetoothsetlocalserviceinfo.htm
tech.root: bltooth
ms.assetid: ab76f5d5-b7b6-4dc5-967d-5fe19260b5ad
ms.date: 12/05/2018
ms.keywords: BluetoothSetLocalServiceInfo, BluetoothSetLocalServiceInfo function [Bluetooth Devices], bltooth.bluetoothsetlocalserviceinfo, bluetoothapis/BluetoothSetLocalServiceInfo, bth_funcs_036c64a4-5050-4d5d-8217-fc4ff9ef300d.xml
req.header: bluetoothapis.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Versions:\_Supported in Windows Vista, and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: BthProps.lib
req.dll: bthprops.cpl; BluetoothAPIs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothSetLocalServiceInfo
 - bluetoothapis/BluetoothSetLocalServiceInfo
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
 - BluetoothSetLocalServiceInfo
---

# BluetoothSetLocalServiceInfo function


## -description

The 
  <b>BluetoothSetLocalServiceInfo</b> function sets local service information for a specific Bluetooth
  radio.

## -parameters

### -param hRadioIn [in, optional]

A handle of the Bluetooth radio device to specify local service information for. If <b>NULL</b>, 
     <b>BluetoothSetLocalServiceInfo</b> searches for the first available local Bluetooth radio.

### -param pClassGuid [in]

The GUID of the service to expose. This should match the <b>GUID</b> in the server-side INF file.

### -param ulInstance [in]

An instance ID for the device node of the Plug and Play (PnP) ID.

### -param pServiceInfoIn [in]

A pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct">BLUETOOTH_LOCAL_SERVICE_INFO</a> structure that describes the local service to
     set.

## -returns

The 
     <b>BluetoothSetLocalServiceInfo</b> function returns the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified Bluetooth radio was not detected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_UNIT</b></dt>
</dl>
</td>
<td width="60%">
No Bluetooth radios were detected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
Sufficient resources were not available to complete the operation. You can receive this error
       when more than 100 local physical device objects (PDOs) correspond to Bluetooth services.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PRIVILEGE_NOT_HELD</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the required privileges. See the Remarks section for information about
       how to elevate privileges.

</td>
</tr>
</table>

## -remarks

<b>BluetoothSetLocalServiceInfo</b> is a user-mode API that is used only by profile driver developers to
    trigger the installation of a local service that is described by the service <b>GUID</b> in 
    <i>pClassGuid</i>.

<b>BluetoothSetLocalServiceInfo</b> generates a Plug and Play (PnP) device ID in the form of "BTHENUM\{<i>ClassGuid</i>}". For example, "BTHENUM\{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". User-mode applications
    can call 
    <b>BluetoothSetLocalServiceInfo</b> subsequent times with the same service GUID but with a different
    instance ID to create multiple instances of the specified server-side profile.

To use Bluetooth APIs like 
    <b>BluetoothSetLocalServiceInfo</b>, user-mode applications should link with 
    BthProps.lib.

<div class="alert"><b>Warning</b>  The process that calls 
    <b>BluetoothSetLocalServiceInfo</b> must have the <b>SE_LOAD_DRIVER_NAME</b> privilege. A process running in the
    system or an administrator context can elevate its privilege by using the SDK 
    <a href="/windows/desktop/api/winbase/nf-winbase-lookupprivilegevaluea">LookupPrivilegeValue</a> and 
    <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> functions. For more information about this see 
    <a href="/previous-versions/ff536681(v=vs.85)">Installing a Bluetooth
    Device</a>.</div>
<div> </div>
The <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct">BLUETOOTH_LOCAL_SERVICE_INFO</a> structure is defined in the SDK 
    BluetoothApis.h header file.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct">BLUETOOTH_LOCAL_SERVICE_INFO</a>