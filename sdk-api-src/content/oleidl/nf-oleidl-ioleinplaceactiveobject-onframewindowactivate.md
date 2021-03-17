---
UID: NF:oleidl.IOleInPlaceActiveObject.OnFrameWindowActivate
title: IOleInPlaceActiveObject::OnFrameWindowActivate (oleidl.h)
description: Notifies the object when the container's top-level frame window is activated or deactivated.
helpviewer_keywords: ["IOleInPlaceActiveObject interface [COM]","OnFrameWindowActivate method","IOleInPlaceActiveObject.OnFrameWindowActivate","IOleInPlaceActiveObject::OnFrameWindowActivate","OnFrameWindowActivate","OnFrameWindowActivate method [COM]","OnFrameWindowActivate method [COM]","IOleInPlaceActiveObject interface","_ole_ioleinplaceactiveobject_onframewindowactivate","com.ioleinplaceactiveobject_onframewindowactivate","oleidl/IOleInPlaceActiveObject::OnFrameWindowActivate"]
old-location: com\ioleinplaceactiveobject_onframewindowactivate.htm
tech.root: com
ms.assetid: 6534ea03-5f1b-4d3e-b6d8-b8d478a0a144
ms.date: 12/05/2018
ms.keywords: IOleInPlaceActiveObject interface [COM],OnFrameWindowActivate method, IOleInPlaceActiveObject.OnFrameWindowActivate, IOleInPlaceActiveObject::OnFrameWindowActivate, OnFrameWindowActivate, OnFrameWindowActivate method [COM], OnFrameWindowActivate method [COM],IOleInPlaceActiveObject interface, _ole_ioleinplaceactiveobject_onframewindowactivate, com.ioleinplaceactiveobject_onframewindowactivate, oleidl/IOleInPlaceActiveObject::OnFrameWindowActivate
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleInPlaceActiveObject::OnFrameWindowActivate
 - oleidl/IOleInPlaceActiveObject::OnFrameWindowActivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceActiveObject.OnFrameWindowActivate
---

# IOleInPlaceActiveObject::OnFrameWindowActivate


## -description

Notifies the object when the container's top-level frame window is activated or deactivated.

## -parameters

### -param fActivate [in]

 The state of the container's top-level frame window. This parameter is <b>TRUE</b> if the window is activating and <b>FALSE</b> if it is deactivating.

## -returns

This method returns S_OK on success.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>