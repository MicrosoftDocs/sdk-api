---
UID: NF:oleidl.IOleInPlaceActiveObject.OnDocWindowActivate
title: IOleInPlaceActiveObject::OnDocWindowActivate (oleidl.h)
description: Notifies the active in-place object when the container's document window is activated or deactivated.
helpviewer_keywords: ["IOleInPlaceActiveObject interface [COM]","OnDocWindowActivate method","IOleInPlaceActiveObject.OnDocWindowActivate","IOleInPlaceActiveObject::OnDocWindowActivate","OnDocWindowActivate","OnDocWindowActivate method [COM]","OnDocWindowActivate method [COM]","IOleInPlaceActiveObject interface","_ole_ioleinplaceactiveobject_ondocwindowactivate","com.ioleinplaceactiveobject_ondocwindowactivate","oleidl/IOleInPlaceActiveObject::OnDocWindowActivate"]
old-location: com\ioleinplaceactiveobject_ondocwindowactivate.htm
tech.root: com
ms.assetid: 8333d707-4d34-4a87-9990-b25597ffa9fc
ms.date: 12/05/2018
ms.keywords: IOleInPlaceActiveObject interface [COM],OnDocWindowActivate method, IOleInPlaceActiveObject.OnDocWindowActivate, IOleInPlaceActiveObject::OnDocWindowActivate, OnDocWindowActivate, OnDocWindowActivate method [COM], OnDocWindowActivate method [COM],IOleInPlaceActiveObject interface, _ole_ioleinplaceactiveobject_ondocwindowactivate, com.ioleinplaceactiveobject_ondocwindowactivate, oleidl/IOleInPlaceActiveObject::OnDocWindowActivate
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
 - IOleInPlaceActiveObject::OnDocWindowActivate
 - oleidl/IOleInPlaceActiveObject::OnDocWindowActivate
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
 - IOleInPlaceActiveObject.OnDocWindowActivate
---

# IOleInPlaceActiveObject::OnDocWindowActivate


## -description

Notifies the active in-place object when the container's document window is activated or deactivated.

## -parameters

### -param fActivate [in]

The state of the MDI child document window. If this parameter is <b>TRUE</b>, the window is in the act of activating; if it is <b>FALSE</b>, it is in the act of deactivating.

## -returns

This method returns S_OK on success.

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call <b>IOleInPlaceActiveObject::OnDocWindowActivate</b> when the MDI child document window is activated or deactivated and the object is currently the active object for the document.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
You should include code in this method that installs frame-level tools during object activation. These tools include the shared composite menu and/or optional toolbars and frame adornments. You should then take focus. When deactivating, the object should remove the frame-level tools. Note that if you do not call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceuiwindow-setborderspace">IOleInPlaceUIWindow::SetBorderSpace</a> with pborderwidths set to <b>NULL</b>, you can avoid having to renegotiate border space.

While executing <b>IOleInPlaceActiveObject::OnDocWindowActivate</b>, do not make calls to the <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <b>IOleInPlaceActiveObject::OnDocWindowActivate</b>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>