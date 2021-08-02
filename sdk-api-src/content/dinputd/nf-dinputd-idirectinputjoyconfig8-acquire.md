---
UID: NF:dinputd.IDirectInputJoyConfig8.Acquire
title: IDirectInputJoyConfig8::Acquire (dinputd.h)
description: The IDirectInputJoyConfig8::Acquire method acquires &quot;joystick configuration mode.&quot; Only one application can be in joystick configuration mode at a time; subsequent attempts by other applications to acquire this mode should receive the error DIERR_OTHERAPPHASPRIO. After entering configuration mode, the application can make alterations to the global joystick configuration settings. The application should check the existing settings before installing the new ones in case another application changed the settings in the interim.
helpviewer_keywords: ["Acquire","Acquire method [Human Input Devices]","Acquire method [Human Input Devices]","IDirectInputJoyConfig8 interface","IDirectInputJoyConfig8 interface [Human Input Devices]","Acquire method","IDirectInputJoyConfig8.Acquire","IDirectInputJoyConfig8::Acquire","di_ref_299a63df-4623-437b-b106-2e8c0530f462.xml","dinputd/IDirectInputJoyConfig8::Acquire","hid.idirectinputjoyconfig8_acquire"]
old-location: hid\idirectinputjoyconfig8_acquire.htm
tech.root: hid
ms.assetid: 1df2eb92-9c55-4371-84c7-a4fb879efb7e
ms.date: 12/05/2018
ms.keywords: Acquire, Acquire method [Human Input Devices], Acquire method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],Acquire method, IDirectInputJoyConfig8.Acquire, IDirectInputJoyConfig8::Acquire, di_ref_299a63df-4623-437b-b106-2e8c0530f462.xml, dinputd/IDirectInputJoyConfig8::Acquire, hid.idirectinputjoyconfig8_acquire
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
 - IDirectInputJoyConfig8::Acquire
 - dinputd/IDirectInputJoyConfig8::Acquire
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
 - IDirectInputJoyConfig8.Acquire
---

# IDirectInputJoyConfig8::Acquire


## -description

The <b>IDirectInputJoyConfig8::Acquire </b> method acquires "joystick configuration mode." Only one application can be in joystick configuration mode at a time; subsequent attempts by other applications  to acquire this mode should receive the error DIERR_OTHERAPPHASPRIO. After entering configuration mode, the application can make alterations to the global joystick configuration settings. The application should check the existing settings before installing the new ones in case another application changed the settings in the interim.



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
<dt><b>DIERR_OTHERAPPHASPRIO </b></dt>
</dl>
</td>
<td width="60%">
Another application is already in joystick configuration mode. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INSUFFICIENTPRIVS </b></dt>
</dl>
</td>
<td width="60%">
The current user does not have the necessary permissions to alter the joystick configuration. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_DEVICECHANGE </b></dt>
</dl>
</td>
<td width="60%">
Another application has changed the global joystick configuration. The interface needs to be reinitialized. 

</td>
</tr>
</table>

