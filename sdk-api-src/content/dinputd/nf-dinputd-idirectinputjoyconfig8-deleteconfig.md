---
UID: NF:dinputd.IDirectInputJoyConfig8.DeleteConfig
title: IDirectInputJoyConfig8::DeleteConfig (dinputd.h)
description: The IDirectInputJoyConfig8::DeleteConfig method deletes configuration information about a joystick.
helpviewer_keywords: ["DeleteConfig","DeleteConfig method [Human Input Devices]","DeleteConfig method [Human Input Devices]","IDirectInputJoyConfig8 interface","IDirectInputJoyConfig8 interface [Human Input Devices]","DeleteConfig method","IDirectInputJoyConfig8.DeleteConfig","IDirectInputJoyConfig8::DeleteConfig","di_ref_453b121d-6edc-4674-ab3c-f610ba900831.xml","dinputd/IDirectInputJoyConfig8::DeleteConfig","hid.idirectinputjoyconfig8_deleteconfig"]
old-location: hid\idirectinputjoyconfig8_deleteconfig.htm
tech.root: hid
ms.assetid: f589e5f4-e003-4a42-b7e6-10b5b14d1aa6
ms.date: 12/05/2018
ms.keywords: DeleteConfig, DeleteConfig method [Human Input Devices], DeleteConfig method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],DeleteConfig method, IDirectInputJoyConfig8.DeleteConfig, IDirectInputJoyConfig8::DeleteConfig, di_ref_453b121d-6edc-4674-ab3c-f610ba900831.xml, dinputd/IDirectInputJoyConfig8::DeleteConfig, hid.idirectinputjoyconfig8_deleteconfig
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
 - IDirectInputJoyConfig8::DeleteConfig
 - dinputd/IDirectInputJoyConfig8::DeleteConfig
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
 - IDirectInputJoyConfig8.DeleteConfig
---

## -description

The <b>IDirectInputJoyConfig8::DeleteConfig </b> method deletes configuration information about a joystick.

## -parameters

### -param unnamedParam1

Indicates a zero-based joystick identification number.

## -returns

Returns DI_OK if successful; otherwise, returns one of the following COM error values (these values are intended to be illustrative and are not necessarily comprehensive): 

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
Joystick configuration has not been acquired. You must call <a href="/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-acquire">IDirectInputJoyConfig8::Acquire</a> before you can alter joystick configuration settings. 

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
</table>