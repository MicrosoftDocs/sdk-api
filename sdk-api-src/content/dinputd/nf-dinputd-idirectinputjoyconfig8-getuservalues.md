---
UID: NF:dinputd.IDirectInputJoyConfig8.GetUserValues
title: IDirectInputJoyConfig8::GetUserValues (dinputd.h)
description: The IDirectInputJoyConfig8::GetUserValues method obtains information about user settings for the joystick.
helpviewer_keywords: ["GetUserValues","GetUserValues method [Human Input Devices]","GetUserValues method [Human Input Devices]","IDirectInputJoyConfig8 interface","IDirectInputJoyConfig8 interface [Human Input Devices]","GetUserValues method","IDirectInputJoyConfig8.GetUserValues","IDirectInputJoyConfig8::GetUserValues","di_ref_91a06462-3eaf-4c52-b6e3-c8598719f048.xml","dinputd/IDirectInputJoyConfig8::GetUserValues","hid.idirectinputjoyconfig8_getuservalues"]
old-location: hid\idirectinputjoyconfig8_getuservalues.htm
tech.root: hid
ms.assetid: b0de6a60-4dab-41a4-a8f7-629dc2795bfe
ms.date: 12/05/2018
ms.keywords: GetUserValues, GetUserValues method [Human Input Devices], GetUserValues method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],GetUserValues method, IDirectInputJoyConfig8.GetUserValues, IDirectInputJoyConfig8::GetUserValues, di_ref_91a06462-3eaf-4c52-b6e3-c8598719f048.xml, dinputd/IDirectInputJoyConfig8::GetUserValues, hid.idirectinputjoyconfig8_getuservalues
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
 - IDirectInputJoyConfig8::GetUserValues
 - dinputd/IDirectInputJoyConfig8::GetUserValues
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
 - IDirectInputJoyConfig8.GetUserValues
---

# IDirectInputJoyConfig8::GetUserValues


## -description

The <b>IDirectInputJoyConfig8::GetUserValues </b> method obtains information about user settings for the joystick.

## -parameters

### -param unnamedParam1

Points to a structure that receives information about the user joystick configuration. The caller must initialize the <b>dwSize</b> member of the <a href="/windows/desktop/api/dinputd/ns-dinputd-dijoyuservalues">DIJOYUSERVALUES</a> structure before calling this method.

### -param unnamedParam2

Specifies which members of the DIJOYUSERVALUES structure contain values to be retrieved. There may be zero, one, or more of the following: 





#### DIJU_USERVALUES

Indicates that the user configuration settings (the <b>ruv</b> member of the DIJOYUSERVALUES structure) is being requested. 



#### DIJU_GLOBALDRIVER

Indicates that the global port driver (the <b>wszGlobalDriver</b> member of the DIJOYUSERVALUES structure) is being requested. 

A list of valid global drivers can be obtained by enumerating the list of joystick types. If the joystick type has the JOY_HWS_ISGAMEPORTDRIVER flag set in the <b>dwFlags</b> member of the JOYHWSETTINGS structure, then the <b>wszCallout</b> member of the <a href="/windows/desktop/api/dinputd/ns-dinputd-dijoytypeinfo">DIJOYTYPEINFO</a> structure contains the name of a driver that can be used as a global driver. 



#### DIJU_GAMEPORTEMULATOR

Unused

## -returns

Returns DI_OK if successful; otherwise, returns the following COM error value: 

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
</table>