---
UID: NF:dinputd.IDirectInputJoyConfig8.GetConfig
title: IDirectInputJoyConfig8::GetConfig (dinputd.h)
description: The IDirectInputJoyConfig8::GetConfig method obtains information about a joystick's configuration.
helpviewer_keywords: ["GetConfig","GetConfig method [Human Input Devices]","GetConfig method [Human Input Devices]","IDirectInputJoyConfig8 interface","IDirectInputJoyConfig8 interface [Human Input Devices]","GetConfig method","IDirectInputJoyConfig8.GetConfig","IDirectInputJoyConfig8::GetConfig","di_ref_86a1c8bf-81df-4c68-b646-347785f3584f.xml","dinputd/IDirectInputJoyConfig8::GetConfig","hid.idirectinputjoyconfig8_getconfig"]
old-location: hid\idirectinputjoyconfig8_getconfig.htm
tech.root: hid
ms.assetid: d8e2a702-d33e-48d2-8e1c-49e09e8f560f
ms.date: 12/05/2018
ms.keywords: GetConfig, GetConfig method [Human Input Devices], GetConfig method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],GetConfig method, IDirectInputJoyConfig8.GetConfig, IDirectInputJoyConfig8::GetConfig, di_ref_86a1c8bf-81df-4c68-b646-347785f3584f.xml, dinputd/IDirectInputJoyConfig8::GetConfig, hid.idirectinputjoyconfig8_getconfig
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
 - IDirectInputJoyConfig8::GetConfig
 - dinputd/IDirectInputJoyConfig8::GetConfig
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
 - IDirectInputJoyConfig8.GetConfig
---

# IDirectInputJoyConfig8::GetConfig


## -description

The <b>IDirectInputJoyConfig8::GetConfig </b> method obtains information about a joystick's configuration.

## -parameters

### -param unnamedParam1

Indicates a joystick identification number. This is a nonnegative integer. To enumerate joysticks, begin with joystick zero and increment the joystick number by one until the function returns DIERR_NOMOREITEMS.

### -param unnamedParam2

Points to a structure that receives information about the joystick configuration. The caller "must" initialize the <b>dwSize</b> member of the <a href="/windows/desktop/api/dinputd/ns-dinputd-dijoyconfig">DIJOYCONFIG</a> structure before calling this method.

### -param unnamedParam3

Specifies the members of the structure pointed to by <i>pjc</i> that are to be filled in.  This parameter can be zero, one, or more of the following: 





#### DIJC_GUIDINSTANCE

Indicates that the instance GUID for the joystick is being requested. An application can pass the instance GUID to <b>IDirectInput::CreateDevice</b> to obtain an <b>IDirectInputDevice</b> interface to the joystick. Note that this flag is not a valid parameter for <b>IDirectInputJoyConfig8::SetConfig</b>. 



#### DIJC_REGHWCONFIGTYPE

Indicates that the hardware configuration for the joystick (the <b>hwc</b> member of the DIJOYCONFIG structure) and the joystick type name (the <b>wszType</b> member of the same structure) are being requested. Note that the hardware configuration and type name cannot be retrieved separately. 



#### DIJC_GAIN

Indicates that the force-feedback gain for the joystick is being requested. 



#### DIJC_CALLOUT

Indicates that the joystick polling callout is being requested.

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
<dt><b>S_FALSE </b></dt>
</dl>
</td>
<td width="60%">
The specified joystick has not yet been configured. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_NOMOREITEMS </b></dt>
</dl>
</td>
<td width="60%">
No more joysticks are available. 

</td>
</tr>
</table>