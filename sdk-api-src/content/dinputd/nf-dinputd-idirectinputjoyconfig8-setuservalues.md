---
UID: NF:dinputd.IDirectInputJoyConfig8.SetUserValues
title: IDirectInputJoyConfig8::SetUserValues (dinputd.h)
description: The IDirectInputJoyConfig8::SetUserValues method sets the user settings for the joystick.
helpviewer_keywords: ["IDirectInputJoyConfig8 interface [Human Input Devices]","SetUserValues method","IDirectInputJoyConfig8.SetUserValues","IDirectInputJoyConfig8::SetUserValues","SetUserValues","SetUserValues method [Human Input Devices]","SetUserValues method [Human Input Devices]","IDirectInputJoyConfig8 interface","di_ref_6630ec2e-5680-4323-b38f-0e9e0ed75761.xml","dinputd/IDirectInputJoyConfig8::SetUserValues","hid.idirectinputjoyconfig8_setuservalues"]
old-location: hid\idirectinputjoyconfig8_setuservalues.htm
tech.root: hid
ms.assetid: 0e33a73b-0315-43a2-8563-f21a7776921c
ms.date: 12/05/2018
ms.keywords: IDirectInputJoyConfig8 interface [Human Input Devices],SetUserValues method, IDirectInputJoyConfig8.SetUserValues, IDirectInputJoyConfig8::SetUserValues, SetUserValues, SetUserValues method [Human Input Devices], SetUserValues method [Human Input Devices],IDirectInputJoyConfig8 interface, di_ref_6630ec2e-5680-4323-b38f-0e9e0ed75761.xml, dinputd/IDirectInputJoyConfig8::SetUserValues, hid.idirectinputjoyconfig8_setuservalues
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
 - IDirectInputJoyConfig8::SetUserValues
 - dinputd/IDirectInputJoyConfig8::SetUserValues
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
 - IDirectInputJoyConfig8.SetUserValues
---

# IDirectInputJoyConfig8::SetUserValues


## -description

The <b>IDirectInputJoyConfig8::SetUserValues </b> method sets the user settings for the joystick.

## -parameters

### -param unnamedParam1

Points to a structure that receives information about the new user joystick settings.

### -param unnamedParam2

Specifies the parts of the <a href="/windows/desktop/api/dinputd/ns-dinputd-dijoyuservalues">DIJOYUSERVALUES</a> structure that contain values to be set.  There may be zero, one, or more of the following: 





#### DIJU_USERVALUES

Indicates that the user configuration settings (the <b>ruv</b> member of the DIJOYUSERVALUES structure) is valid. 



#### DIJU_GLOBALDRIVER

Indicates that the global port driver (the <b>wszGlobalDriver</b> member of the DIJOYUSERVALUES structure) is valid. 

A list of valid global drivers can be obtained by enumerating the list of joystick types. If the joystick type has the JOY_HWS_ISGAMEPORTDRIVER flag set in the <b>dwFlags</b> member of the JOYHWSETTINGS structure, then the <b>wszCallout</b> member of the <a href="/windows/desktop/api/dinputd/ns-dinputd-dijoytypeinfo">DIJOYTYPEINFO</a> structure contains the name of a driver that can be used as a global driver. 



#### DIJU_GAMEPORTEMULATOR

Unused.

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