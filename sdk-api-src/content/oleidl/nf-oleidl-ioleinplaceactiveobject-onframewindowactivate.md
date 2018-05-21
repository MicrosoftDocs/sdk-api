---
UID: NF:oleidl.IOleInPlaceActiveObject.OnFrameWindowActivate
title: IOleInPlaceActiveObject::OnFrameWindowActivate
author: windows-driver-content
description: Notifies the object when the container's top-level frame window is activated or deactivated.
old-location: com\ioleinplaceactiveobject_onframewindowactivate.htm
old-project: com
ms.assetid: 6534ea03-5f1b-4d3e-b6d8-b8d478a0a144
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IOleInPlaceActiveObject interface [COM],OnFrameWindowActivate method, IOleInPlaceActiveObject.OnFrameWindowActivate, IOleInPlaceActiveObject::OnFrameWindowActivate, OnFrameWindowActivate, OnFrameWindowActivate method [COM], OnFrameWindowActivate method [COM],IOleInPlaceActiveObject interface, _ole_ioleinplaceactiveobject_onframewindowactivate, com.ioleinplaceactiveobject_onframewindowactivate, oleidl/IOleInPlaceActiveObject::OnFrameWindowActivate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleInPlaceActiveObject.OnFrameWindowActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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




<a href="_win32_GetMessage_cpp">GetMessage</a>



<a href="https://msdn.microsoft.com/b077c256-1109-494c-95c2-2d33bccbe47b">IOleInPlaceActiveObject</a>



<a href="_win32_PeekMessage_cpp">PeekMessage</a>
 

 

