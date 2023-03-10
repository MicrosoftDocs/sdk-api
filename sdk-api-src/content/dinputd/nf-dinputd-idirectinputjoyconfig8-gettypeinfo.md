---
UID: NF:dinputd.IDirectInputJoyConfig8.GetTypeInfo
title: IDirectInputJoyConfig8::GetTypeInfo (dinputd.h)
description: The IDirectInputJoyConfig8::GetTypeInfo method obtains information about a joystick type.
helpviewer_keywords: ["GetTypeInfo","GetTypeInfo method [Human Input Devices]","GetTypeInfo method [Human Input Devices]","IDirectInputJoyConfig8 interface","IDirectInputJoyConfig8 interface [Human Input Devices]","GetTypeInfo method","IDirectInputJoyConfig8.GetTypeInfo","IDirectInputJoyConfig8::GetTypeInfo","di_ref_9e378bd2-ae1a-4a66-b934-d9d5ad46cf5d.xml","dinputd/IDirectInputJoyConfig8::GetTypeInfo","hid.idirectinputjoyconfig8_gettypeinfo"]
old-location: hid\idirectinputjoyconfig8_gettypeinfo.htm
tech.root: hid
ms.assetid: e850c3a4-b2dd-4de5-82e3-5bbd90a7ba15
ms.date: 12/05/2018
ms.keywords: GetTypeInfo, GetTypeInfo method [Human Input Devices], GetTypeInfo method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],GetTypeInfo method, IDirectInputJoyConfig8.GetTypeInfo, IDirectInputJoyConfig8::GetTypeInfo, di_ref_9e378bd2-ae1a-4a66-b934-d9d5ad46cf5d.xml, dinputd/IDirectInputJoyConfig8::GetTypeInfo, hid.idirectinputjoyconfig8_gettypeinfo
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
 - IDirectInputJoyConfig8::GetTypeInfo
 - dinputd/IDirectInputJoyConfig8::GetTypeInfo
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
 - IDirectInputJoyConfig8.GetTypeInfo
---

# IDirectInputJoyConfig8::GetTypeInfo


## -description

The <b>IDirectInputJoyConfig8::GetTypeInfo </b> method obtains information about a joystick type.

## -parameters

### -param unnamedParam1

Points to the name of the type, previously obtained from a call to <a href="/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-enumtypes">IDirectInputJoyConfig8::EnumTypes</a>.

### -param unnamedParam2

Points to a structure that receives information about the joystick type. The caller must initialize the <b>dwSize</b> member of the <a href="/windows/desktop/api/dinputd/ns-dinputd-dijoytypeinfo">DIJOYTYPEINFO</a> structure before calling this method.

### -param unnamedParam3

Specifies the parts of the DIJOYTYPEINFO structure pointed to by <i>pjti</i> that are to be filled. There may be zero, one, or more of the following: 





#### DITC_REGHWSETTINGS

Indicates that the registry hardware settings for the joystick are being requested. 



#### DITC_CLSIDCONFIG

Indicates that the joystick configuration CLSID is being requested. If the value is all zeros, then there is no custom configuration for this joystick type. 



#### DITC_DISPLAYNAME

Indicates that the display name for the joystick type is being requested. 



#### DITC_CALLOUT

Indicates that the callout for the joystick type is being requested.

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
<dt><b>DIERR_NOTFOUND </b></dt>
</dl>
</td>
<td width="60%">
The joystick type was not found. 

</td>
</tr>
</table>