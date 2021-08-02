---
UID: NF:dinputd.IDirectInputJoyConfig8.DeleteType
title: IDirectInputJoyConfig8::DeleteType (dinputd.h)
description: The IDirectInputJoyConfig8::DeleteType method removes information about a joystick type. Use this method with caution; it is the caller's responsibility to ensure that no joystick refers to the deleted type.
helpviewer_keywords: ["DeleteType","DeleteType method [Human Input Devices]","DeleteType method [Human Input Devices]","IDirectInputJoyConfig8 interface","IDirectInputJoyConfig8 interface [Human Input Devices]","DeleteType method","IDirectInputJoyConfig8.DeleteType","IDirectInputJoyConfig8::DeleteType","di_ref_09e54785-5e07-4eba-bcd7-a3e016923ae3.xml","dinputd/IDirectInputJoyConfig8::DeleteType","hid.idirectinputjoyconfig8_deletetype"]
old-location: hid\idirectinputjoyconfig8_deletetype.htm
tech.root: hid
ms.assetid: 6e1628c4-1d4f-4751-acac-7a309a99aedb
ms.date: 12/05/2018
ms.keywords: DeleteType, DeleteType method [Human Input Devices], DeleteType method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],DeleteType method, IDirectInputJoyConfig8.DeleteType, IDirectInputJoyConfig8::DeleteType, di_ref_09e54785-5e07-4eba-bcd7-a3e016923ae3.xml, dinputd/IDirectInputJoyConfig8::DeleteType, hid.idirectinputjoyconfig8_deletetype
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
 - IDirectInputJoyConfig8::DeleteType
 - dinputd/IDirectInputJoyConfig8::DeleteType
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
 - IDirectInputJoyConfig8.DeleteType
---

## -description

The <b>IDirectInputJoyConfig8::DeleteType </b> method removes information about a joystick type. Use this method with caution; it is the caller's responsibility to ensure that no joystick refers to the deleted type.

## -parameters

### -param unnamedParam1

Points to the name of the type. The name of the type cannot exceed MAX_PATH characters, including the terminating null character. Also, the name cannot begin with a "#" character. Types beginning with "#" are reserved by DirectInput.

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