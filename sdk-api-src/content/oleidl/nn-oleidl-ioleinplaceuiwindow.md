---
UID: NN:oleidl.IOleInPlaceUIWindow
title: IOleInPlaceUIWindow (oleidl.h)
description: Implemented by container applications and used by object applications to negotiate border space on the document or frame window.
helpviewer_keywords: ["IOleInPlaceUIWindow","IOleInPlaceUIWindow interface [COM]","IOleInPlaceUIWindow interface [COM]","described","_ole_ioleinplaceuiwindow","com.ioleinplaceuiwindow","oleidl/IOleInPlaceUIWindow"]
old-location: com\ioleinplaceuiwindow.htm
tech.root: com
ms.assetid: 3cfb31aa-9746-438c-af64-8236c170fe88
ms.date: 12/05/2018
ms.keywords: IOleInPlaceUIWindow, IOleInPlaceUIWindow interface [COM], IOleInPlaceUIWindow interface [COM],described, _ole_ioleinplaceuiwindow, com.ioleinplaceuiwindow, oleidl/IOleInPlaceUIWindow
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
 - IOleInPlaceUIWindow
 - oleidl/IOleInPlaceUIWindow
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
 - IOleInPlaceUIWindow
---

# IOleInPlaceUIWindow interface


## -description

Implemented by container applications and used by object applications to negotiate border space on the document or frame window. The container provides a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure in which the object can place toolbars and other similar controls, determines if tools can in fact be installed around the object's window frame, allocates space for the border, and establishes a communication channel between the object and each frame and document window.

## -inheritance

The <b>IOleInPlaceUIWindow</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IOleInPlaceUIWindow</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>
