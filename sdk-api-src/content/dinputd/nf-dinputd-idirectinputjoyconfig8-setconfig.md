---
UID: NF:dinputd.IDirectInputJoyConfig8.SetConfig
title: IDirectInputJoyConfig8::SetConfig (dinputd.h)
description: The IDirectInputJoyConfig8::SetConfig method creates or redefines configuration information about a joystick.
helpviewer_keywords: ["IDirectInputJoyConfig8 interface [Human Input Devices]","SetConfig method","IDirectInputJoyConfig8.SetConfig","IDirectInputJoyConfig8::SetConfig","SetConfig","SetConfig method [Human Input Devices]","SetConfig method [Human Input Devices]","IDirectInputJoyConfig8 interface","di_ref_e9168f2d-cee8-4cac-8299-65360fd784f1.xml","dinputd/IDirectInputJoyConfig8::SetConfig","hid.idirectinputjoyconfig8_setconfig"]
old-location: hid\idirectinputjoyconfig8_setconfig.htm
tech.root: hid
ms.assetid: 58f413c4-7b4c-47bd-8991-ffe681e96f48
ms.date: 12/05/2018
ms.keywords: IDirectInputJoyConfig8 interface [Human Input Devices],SetConfig method, IDirectInputJoyConfig8.SetConfig, IDirectInputJoyConfig8::SetConfig, SetConfig, SetConfig method [Human Input Devices], SetConfig method [Human Input Devices],IDirectInputJoyConfig8 interface, di_ref_e9168f2d-cee8-4cac-8299-65360fd784f1.xml, dinputd/IDirectInputJoyConfig8::SetConfig, hid.idirectinputjoyconfig8_setconfig
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
 - IDirectInputJoyConfig8::SetConfig
 - dinputd/IDirectInputJoyConfig8::SetConfig
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
 - IDirectInputJoyConfig8.SetConfig
---

# IDirectInputJoyConfig8::SetConfig


## -description

The <b>IDirectInputJoyConfig8::SetConfig </b> method creates or redefines configuration information about a joystick.

## -parameters

### -param unnamedParam1

Indicates a zero-based joystick identification number.

### -param unnamedParam2

Contains information about the joystick.

### -param unnamedParam3

Specifies the parts of the <a href="/windows/desktop/api/dinputd/ns-dinputd-dijoyconfig">DIJOYCONFIG</a> structure pointed to by <i>pcfg</i> that contain information to be set. There may be zero, one, or more of the following: 





#### DIJC_REGHWCONFIGTYPE

Indicates that the hardware configuration for the joystick (the <b>hwc</b> member of the DIJOYCONFIG structure) and the joystick type name (the <b>wszType</b> member of the DIJOYCONFIG) are valid. Note that the hardware configuration and type name cannot be set separately. 



#### DIJC_GAIN

Indicates that the force-feedback gain for the joystick is valid. 



#### DIJC_CALLOUT

Indicates that the joystick polling callout is valid.

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
Joystick configuration has not been acquired. You must call <a href="/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-acquire">IDirectInputJoyConfig8::Acquire</a> before you can notify applications and drivers of changes to joystick configuration. 

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