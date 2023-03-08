---
UID: NF:dinputd.IDirectInputJoyConfig.OpenConfigKey
title: IDirectInputJoyConfig::OpenConfigKey (dinputd.h)
description: The IDirectInputJoyConfig8::OpenConfigKey method opens IDirectInputJoyConfig the registry key associated with a joystick configuration.
helpviewer_keywords: ["IDirectInputJoyConfig interface [Human Input Devices]","OpenConfigKey method","IDirectInputJoyConfig.OpenConfigKey","IDirectInputJoyConfig::OpenConfigKey","OpenConfigKey","OpenConfigKey (IDirectInputJoyConfig8)","OpenConfigKey method [Human Input Devices]","OpenConfigKey method [Human Input Devices]","IDirectInputJoyConfig interface","di_ref_d0c78a58-7e2c-46bb-a974-4996a2e488a3.xml","dinputd/IDirectInputJoyConfig::OpenConfigKey","hid.idirectinputjoyconfig8_openconfigkey"]
old-location: hid\idirectinputjoyconfig8_openconfigkey.htm
tech.root: hid
ms.assetid: f3e902e1-bc5d-419e-b728-2f9199dacb94
ms.date: 12/05/2018
ms.keywords: IDirectInputJoyConfig interface [Human Input Devices],OpenConfigKey method, IDirectInputJoyConfig.OpenConfigKey, IDirectInputJoyConfig::OpenConfigKey, OpenConfigKey, OpenConfigKey (IDirectInputJoyConfig8), OpenConfigKey method [Human Input Devices], OpenConfigKey method [Human Input Devices],IDirectInputJoyConfig interface, di_ref_d0c78a58-7e2c-46bb-a974-4996a2e488a3.xml, dinputd/IDirectInputJoyConfig::OpenConfigKey, hid.idirectinputjoyconfig8_openconfigkey
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
 - IDirectInputJoyConfig::OpenConfigKey
 - dinputd/IDirectInputJoyConfig::OpenConfigKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dinputd.h
api_name:
 - IDirectInputJoyConfig.OpenConfigKey
---

# IDirectInputJoyConfig::OpenConfigKey


## -description

The <b>IDirectInputJoyConfig8::OpenConfigKey </b> method opens IDirectInputJoyConfig the registry key associated with a joystick configuration. Control panel applications can use this key to store per-joystick persistent information, such as button mappings. Such private information should be kept in a subkey named <b>OEM</b>; do not store private information in the main configuration key. The application should use <b>RegCloseKey</b> to close the registry key.

## -parameters

### -param unnamedParam1

Indicates a zero-based joystick identification number.

### -param unnamedParam2

Specifies a registry security access mask. This can be any of the values permitted by the <b>RegOpenKeyEx</b> function. If write access is requested, then joystick configuration must first be acquired. If only read access is requested, then acquisition is not required. At least one access mask must be specified.

### -param unnamedParam3

Points to the opened registry key on success.

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
<dt><b>DIERR_NOTFOUND </b></dt>
</dl>
</td>
<td width="60%">
The application attempted to open the configuration key for reading, but no configuration key for the joystick had been created. Applications should proceed as if the key were empty. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAKE_HRESULT(SEVERITY_ERROR, FACILITY_WIN32, ErrorCode) </b></dt>
</dl>
</td>
<td width="60%">
A Win32 error code if access to the key is denied because of inappropriate registry permissions or some other external factor. 

</td>
</tr>
</table>