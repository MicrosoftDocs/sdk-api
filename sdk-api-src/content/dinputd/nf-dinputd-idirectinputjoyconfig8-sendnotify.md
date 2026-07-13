---
UID: NF:dinputd.IDirectInputJoyConfig8.SendNotify
title: IDirectInputJoyConfig8::SendNotify (dinputd.h)
description: The IDirectInputJoyConfig8::SendNotify method notifies device drivers and applications that changes to the device configuration have been made.
helpviewer_keywords: ["IDirectInputJoyConfig8 interface [Human Input Devices]","SendNotify method","IDirectInputJoyConfig8.SendNotify","IDirectInputJoyConfig8::SendNotify","SendNotify","SendNotify method [Human Input Devices]","SendNotify method [Human Input Devices]","IDirectInputJoyConfig8 interface","di_ref_0dc1b65b-edf9-409c-8611-cf3aee61e28a.xml","dinputd/IDirectInputJoyConfig8::SendNotify","hid.idirectinputjoyconfig8_sendnotify"]
old-location: hid\idirectinputjoyconfig8_sendnotify.htm
tech.root: hid
ms.assetid: 8ca09ce2-82cc-4aee-be96-5123cb0f1f3a
ms.date: 12/05/2018
ms.keywords: IDirectInputJoyConfig8 interface [Human Input Devices],SendNotify method, IDirectInputJoyConfig8.SendNotify, IDirectInputJoyConfig8::SendNotify, SendNotify, SendNotify method [Human Input Devices], SendNotify method [Human Input Devices],IDirectInputJoyConfig8 interface, di_ref_0dc1b65b-edf9-409c-8611-cf3aee61e28a.xml, dinputd/IDirectInputJoyConfig8::SendNotify, hid.idirectinputjoyconfig8_sendnotify
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
 - IDirectInputJoyConfig8::SendNotify
 - dinputd/IDirectInputJoyConfig8::SendNotify
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
 - IDirectInputJoyConfig8.SendNotify
---

# IDirectInputJoyConfig8::SendNotify


## -description

The <b>IDirectInputJoyConfig8::SendNotify </b> method notifies device drivers and applications that changes to the device configuration have been made. An application that changes device configurations must invoke this method after the changes have been made (and before unacquiring the device).



## -returns

Returns DI_OK if successful; otherwise, returns the following COM error value (this value is intended to be illustrative and is not necessarily comprehensive): 

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
</table>
