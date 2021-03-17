---
UID: NF:directmanipulation.IDirectManipulationViewport.SetContact
title: IDirectManipulationViewport::SetContact (directmanipulation.h)
description: Specifies an association between a contact and the viewport.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","SetContact method","IDirectManipulationViewport.SetContact","IDirectManipulationViewport::SetContact","SetContact","SetContact method [Direct Manipulation]","SetContact method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_setcontact","directmanipulation/IDirectManipulationViewport::SetContact"]
old-location: directmanipulation\idirectmanipulationviewport_setcontact.htm
tech.root: directmanipulation
ms.assetid: 39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetContact method, IDirectManipulationViewport.SetContact, IDirectManipulationViewport::SetContact, SetContact, SetContact method [Direct Manipulation], SetContact method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setcontact, directmanipulation/IDirectManipulationViewport::SetContact
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - IDirectManipulationViewport::SetContact
 - directmanipulation/IDirectManipulationViewport::SetContact
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.SetContact
---

# IDirectManipulationViewport::SetContact


## -description

Specifies an  association between a contact and the viewport.

## -parameters

### -param pointerId [in]

The ID of the pointer.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method when a <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> message is received. Upon receiving a <b>WM_POINTERDOWN</b>, the application can use the coordinates of the input to hit-test and determine the viewports to which the contact is associated.



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact">DeferContact</a> must be called before <b>SetContact</b>.

After initialization, <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> is not aware of viewport z-order or parent-child relations between viewports. The order of <b>SetContact</b> calls defines the viewport tree. To establish the correct viewport hierarchy, <b>SetContact</b> should be called first on the child-most viewport, followed by the parent, grand-parent, and so on. 


Use <a href="/windows/desktop/api/winuser/nf-winuser-get_pointerid_wparam">GET_POINTERID_WPARAM</a> to get the pointer identifier from a pointer message. The contact is removed automatically when <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerup">WM_POINTERUP</a> is received.


If a contact is associated with one or more viewports using the <b>SetContact</b> method, <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> will examine further input from that contact and attempt to identify an appropriate manipulation based on the configuration of the associated viewports. If a manipulation is recognized, the application will then receive a <a href="/previous-versions/windows/desktop/inputmsg/wm-pointercapturechanged">WM_POINTERCAPTURECHANGED</a> message for this contact. In this context, the <b>WM_POINTERCAPTURECHANGED</b> message indicates that Direct Manipulation has captured the contact and the application will not receive input from this contact that is consumed for this manipulation.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>



<a href="/previous-versions/windows/desktop/inputmsg/messages-and-notifications">User Input Messages and Notifications</a>