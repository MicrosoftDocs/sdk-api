---
UID: NF:dinputd.IDirectInputJoyConfig8.OpenTypeKey
title: IDirectInputJoyConfig8::OpenTypeKey (dinputd.h)
description: The IDirectInputJoyConfig8::OpenTypeKey method opens the registry key associated with a joystick type.
helpviewer_keywords: ["IDirectInputJoyConfig8 interface [Human Input Devices]","OpenTypeKey method","IDirectInputJoyConfig8.OpenTypeKey","IDirectInputJoyConfig8::OpenTypeKey","OpenTypeKey","OpenTypeKey method [Human Input Devices]","OpenTypeKey method [Human Input Devices]","IDirectInputJoyConfig8 interface","di_ref_073c7914-daaf-4db5-95bc-2fd2aef897b5.xml","dinputd/IDirectInputJoyConfig8::OpenTypeKey","hid.idirectinputjoyconfig8_opentypekey"]
old-location: hid\idirectinputjoyconfig8_opentypekey.htm
tech.root: hid
ms.assetid: d747625b-a9e3-41cb-894a-1f62599c62a9
ms.date: 12/05/2018
ms.keywords: IDirectInputJoyConfig8 interface [Human Input Devices],OpenTypeKey method, IDirectInputJoyConfig8.OpenTypeKey, IDirectInputJoyConfig8::OpenTypeKey, OpenTypeKey, OpenTypeKey method [Human Input Devices], OpenTypeKey method [Human Input Devices],IDirectInputJoyConfig8 interface, di_ref_073c7914-daaf-4db5-95bc-2fd2aef897b5.xml, dinputd/IDirectInputJoyConfig8::OpenTypeKey, hid.idirectinputjoyconfig8_opentypekey
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectInputJoyConfig8::OpenTypeKey
 - dinputd/IDirectInputJoyConfig8::OpenTypeKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputJoyConfig8.OpenTypeKey
---

# IDirectInputJoyConfig8::OpenTypeKey


## -description

The <b>IDirectInputJoyConfig8::OpenTypeKey </b> method opens the registry key associated with a joystick type.

## -parameters

### -param unnamedParam1

Points to the name of the type. The name of the type cannot exceed MAX_PATH characters, including the terminating null character. The name cannot begin with a "#" character. Types beginning with "#" are reserved by DirectInput.

### -param unnamedParam2

Specifies a registry security access mask. This can be any of the values permitted by the <b>RegOpenKeyEx</b> function. If write access is requested, then joystick configuration must first have been acquired. If only read access is requested, then acquisition is not required.

### -param unnamedParam3

Points to the opened registry key, on success.

## -returns

Returns DI_OK if successful; otherwise, returns one of the following COM error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_NOTACQUIRED </b></dt>
</dl>
</td>
<td width="60%">
Joystick configuration has not been acquired. You must call <a href="/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-acquire">IDirectInputJoyConfig8::Acquire</a> before you can open a joystick type configuration key for writing. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INVALIDPARAM </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters was invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAKE_HRESULT(SEVERITY_ERROR, FACILITY_WIN32, ErrorCode) </b></dt>
</dl>
</td>
<td width="60%">
A Win32 error code if access to the key is denied by registry permissions or some other external factor. 

</td>
</tr>
</table>

## -remarks

Control panel applications can use the registry key opened by this method to store per-type persistent information, such as global configuration parameters. Such private information should be kept in a subkey named <b>OEM</b>; do not store private information in the main type key. Control panel applications can also use this key to read configuration information, such as the strings to use for device calibration prompts. The application should use <b>RegCloseKey</b> to close the registry key.