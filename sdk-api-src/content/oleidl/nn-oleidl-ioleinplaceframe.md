---
UID: NN:oleidl.IOleInPlaceFrame
title: IOleInPlaceFrame (oleidl.h)
description: Controls the container's top-level frame window.
helpviewer_keywords: ["IOleInPlaceFrame","IOleInPlaceFrame interface [COM]","IOleInPlaceFrame interface [COM]","described","_ole_ioleinplaceframe","com.ioleinplaceframe","oleidl/IOleInPlaceFrame"]
old-location: com\ioleinplaceframe.htm
tech.root: com
ms.assetid: c530aff7-fd83-413d-8945-0c9d1bfb51ba
ms.date: 12/05/2018
ms.keywords: IOleInPlaceFrame, IOleInPlaceFrame interface [COM], IOleInPlaceFrame interface [COM],described, _ole_ioleinplaceframe, com.ioleinplaceframe, oleidl/IOleInPlaceFrame
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
 - IOleInPlaceFrame
 - oleidl/IOleInPlaceFrame
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
 - IOleInPlaceFrame
---

# IOleInPlaceFrame interface


## -description

Controls the container's top-level frame window. This control involves allowing the container to insert its menu group into the composite menu, install the composite menu into the appropriate window frame, and remove the container's menu elements from the composite menu. It sets and displays status text relevant to the in-place object. It also enables or disables the frame's modeless dialog boxes, and translates accelerator keystrokes intended for the container's frame.

## -inheritance

The <b>IOleInPlaceFrame</b> interface inherits from <b>IOleInPlaceUIWindow</b>. <b>IOleInPlaceFrame</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>
