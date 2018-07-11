---
UID: NF:oleidl.IOleInPlaceActiveObject.OnDocWindowActivate
title: IOleInPlaceActiveObject::OnDocWindowActivate
author: windows-sdk-content
description: Notifies the active in-place object when the container's document window is activated or deactivated.
old-location: com\ioleinplaceactiveobject_ondocwindowactivate.htm
old-project: com
ms.assetid: 8333d707-4d34-4a87-9990-b25597ffa9fc
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IOleInPlaceActiveObject interface [COM],OnDocWindowActivate method, IOleInPlaceActiveObject.OnDocWindowActivate, IOleInPlaceActiveObject::OnDocWindowActivate, OnDocWindowActivate, OnDocWindowActivate method [COM], OnDocWindowActivate method [COM],IOleInPlaceActiveObject interface, _ole_ioleinplaceactiveobject_ondocwindowactivate, com.ioleinplaceactiveobject_ondocwindowactivate, oleidl/IOleInPlaceActiveObject::OnDocWindowActivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceActiveObject.OnDocWindowActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
You should include code in this method that installs frame-level tools during object activation. These tools include the shared composite menu and/or optional toolbars and frame adornments. You should then take focus. When deactivating, the object should remove the frame-level tools. Note that if you do not call <a href="https://msdn.microsoft.com/7c806a02-db6d-444e-a049-22c4ae2b19b0">IOleInPlaceUIWindow::SetBorderSpace</a> with pborderwidths set to <b>NULL</b>, you can avoid having to renegotiate border space.

While executing <b>IOleInPlaceActiveObject::OnDocWindowActivate</b>, do not make calls to the <a href="_win32_PeekMessage_cpp">PeekMessage</a> or <a href="_win32_GetMessage_cpp">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <b>IOleInPlaceActiveObject::OnDocWindowActivate</b>.




## -see-also




<a href="_win32_GetMessage_cpp">GetMessage</a>



<a href="https://msdn.microsoft.com/b077c256-1109-494c-95c2-2d33bccbe47b">IOleInPlaceActiveObject</a>



<a href="_win32_PeekMessage_cpp">PeekMessage</a>
 

 

