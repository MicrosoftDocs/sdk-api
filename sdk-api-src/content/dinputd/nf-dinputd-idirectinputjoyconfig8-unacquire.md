---
UID: NF:dinputd.IDirectInputJoyConfig8.Unacquire
title: IDirectInputJoyConfig8::Unacquire (dinputd.h)
description: The IDirectInputJoyConfig8::Unacquire method unacquires &quot;joystick configuration mode&quot;.
helpviewer_keywords: ["IDirectInputJoyConfig8 interface [Human Input Devices]","Unacquire method","IDirectInputJoyConfig8.Unacquire","IDirectInputJoyConfig8::Unacquire","Unacquire","Unacquire method [Human Input Devices]","Unacquire method [Human Input Devices]","IDirectInputJoyConfig8 interface","di_ref_df66f848-ee07-47f7-afc3-3f1d2883c070.xml","dinputd/IDirectInputJoyConfig8::Unacquire","hid.idirectinputjoyconfig8_unacquire"]
old-location: hid\idirectinputjoyconfig8_unacquire.htm
tech.root: hid
ms.assetid: d6eb4743-5845-4acd-8526-f2ab562aa24f
ms.date: 12/05/2018
ms.keywords: IDirectInputJoyConfig8 interface [Human Input Devices],Unacquire method, IDirectInputJoyConfig8.Unacquire, IDirectInputJoyConfig8::Unacquire, Unacquire, Unacquire method [Human Input Devices], Unacquire method [Human Input Devices],IDirectInputJoyConfig8 interface, di_ref_df66f848-ee07-47f7-afc3-3f1d2883c070.xml, dinputd/IDirectInputJoyConfig8::Unacquire, hid.idirectinputjoyconfig8_unacquire
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
 - IDirectInputJoyConfig8::Unacquire
 - dinputd/IDirectInputJoyConfig8::Unacquire
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
 - IDirectInputJoyConfig8.Unacquire
---

# IDirectInputJoyConfig8::Unacquire


## -description

The <b>IDirectInputJoyConfig8::Unacquire </b> method unacquires "joystick configuration mode".



## -returns

Returns DI_OK if successful; otherwise, returns a COM error code.

## -remarks

Before unacquiring configuration mode, the application performs an <a href="/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-sendnotify">IDirectInputJoyConfig8::SendNotify</a> to propagate the changes in the joystick configuration to all device drivers and applications. Applications that hold interfaces to a joystick that is materially affected by a change in configuration should receive the DIERR_DEVICECHANGE error code until the device is reinitialized. Examples of material changes to configuration include altering the number of axes or the number of buttons. In comparison, changes to device calibration are handled internally by DirectInput and are transparent to the application.
