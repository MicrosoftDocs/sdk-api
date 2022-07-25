---
UID: NN:ocidl.IOleInPlaceSiteEx
title: IOleInPlaceSiteEx (ocidl.h)
description: Provides an additional set of activation and deactivation notification methods that enable an object to avoid unnecessary flashing on the screen when the object is activated and deactivated.
helpviewer_keywords: ["IOleInPlaceSiteEx","IOleInPlaceSiteEx interface [COM]","IOleInPlaceSiteEx interface [COM]","described","_ole_ioleinplacesiteex","com.ioleinplacesiteex","ocidl/IOleInPlaceSiteEx"]
old-location: com\ioleinplacesiteex.htm
tech.root: com
ms.assetid: d93e6d23-7867-43e4-8ab9-efe609362c18
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteEx, IOleInPlaceSiteEx interface [COM], IOleInPlaceSiteEx interface [COM],described, _ole_ioleinplacesiteex, com.ioleinplacesiteex, ocidl/IOleInPlaceSiteEx
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
 - IOleInPlaceSiteEx
 - ocidl/IOleInPlaceSiteEx
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
 - IOleInPlaceSiteEx
---

# IOleInPlaceSiteEx interface


## -description

Provides an additional set of activation and deactivation notification methods that enable an object to avoid unnecessary flashing on the screen when the object is activated and deactivated.

When an object is activated, it does not know if its visual display is already correct. When the object is deactivated, the container does not know if the visual display is correct. To avoid a redraw and the associated screen flicker in both cases, the container can provide this extension to <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>.

## -inheritance

The <b>IOleInPlaceSiteEx</b> interface inherits from <b>IOleInPlaceSite</b>. <b>IOleInPlaceSiteEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
