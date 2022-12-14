---
UID: NN:ocidl.IOleInPlaceSiteWindowless
title: IOleInPlaceSiteWindowless (ocidl.h)
description: Extends the IOleInPlaceSiteEx interface.
helpviewer_keywords: ["IOleInPlaceSiteWindowless","IOleInPlaceSiteWindowless interface [COM]","IOleInPlaceSiteWindowless interface [COM]","described","_ole_ioleinplacesitewindowless","com.ioleinplacesitewindowless","ocidl/IOleInPlaceSiteWindowless"]
old-location: com\ioleinplacesitewindowless.htm
tech.root: com
ms.assetid: 4ad83599-99d2-4b35-95de-cff845a8d5e4
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteWindowless, IOleInPlaceSiteWindowless interface [COM], IOleInPlaceSiteWindowless interface [COM],described, _ole_ioleinplacesitewindowless, com.ioleinplacesitewindowless, ocidl/IOleInPlaceSiteWindowless
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IOleInPlaceSiteWindowless
 - ocidl/IOleInPlaceSiteWindowless
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleInPlaceSiteWindowless
---

# IOleInPlaceSiteWindowless interface


## -description

Extends the <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesiteex">IOleInPlaceSiteEx</a> interface. <b>IOleInPlaceSiteWindowless</b> works with <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a> which is implemented on the windowless object. Together, these two interfaces provide services to a windowless object from its container allowing the windowless object to:
<ul>
<li>Process window messages</li>
<li>Participate in drag and drop operations
</li>
<li>Perform drawing operations</li>
</ul>Having a window can place unnecessary burdens on small objects, such as controls. It prevents an object from being non-rectangular. It prevents windows from being transparent. It prevents the small instance size needed by many small controls.

A windowless object can enter the in-place active state without requiring a window or the resources associated with a window. Instead, the object's container provides the object with many of the services associated with having a window.

## -inheritance

The <b>IOleInPlaceSiteWindowless</b> interface inherits from <b>IOleInPlaceSiteEx</b>. <b>IOleInPlaceSiteWindowless</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iadvisesinkex">IAdviseSinkEx</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrol">IOleControl</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-translateaccelerator">IOleInPlaceActiveObject::TranslateAccelerator</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a>
