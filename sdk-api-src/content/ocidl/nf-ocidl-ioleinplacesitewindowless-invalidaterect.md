---
UID: NF:ocidl.IOleInPlaceSiteWindowless.InvalidateRect
title: IOleInPlaceSiteWindowless::InvalidateRect (ocidl.h)
description: Enables an object to invalidate a specified rectangle of its in-place image on the screen.
helpviewer_keywords: ["IOleInPlaceSiteWindowless interface [COM]","InvalidateRect method","IOleInPlaceSiteWindowless.InvalidateRect","IOleInPlaceSiteWindowless::InvalidateRect","InvalidateRect","InvalidateRect method [COM]","InvalidateRect method [COM]","IOleInPlaceSiteWindowless interface","_ole_ioleinplacesitewindowless_invalidaterect","com.ioleinplacesitewindowless_invalidaterect","ocidl/IOleInPlaceSiteWindowless::InvalidateRect"]
old-location: com\ioleinplacesitewindowless_invalidaterect.htm
tech.root: com
ms.assetid: 034025f5-f9cd-4ad3-9b98-216b373cd10f
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteWindowless interface [COM],InvalidateRect method, IOleInPlaceSiteWindowless.InvalidateRect, IOleInPlaceSiteWindowless::InvalidateRect, InvalidateRect, InvalidateRect method [COM], InvalidateRect method [COM],IOleInPlaceSiteWindowless interface, _ole_ioleinplacesitewindowless_invalidaterect, com.ioleinplacesitewindowless_invalidaterect, ocidl/IOleInPlaceSiteWindowless::InvalidateRect
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
 - IOleInPlaceSiteWindowless::InvalidateRect
 - ocidl/IOleInPlaceSiteWindowless::InvalidateRect
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
 - IOleInPlaceSiteWindowless.InvalidateRect
---

# IOleInPlaceSiteWindowless::InvalidateRect


## -description

Enables an object to invalidate a specified rectangle of its in-place image on the screen.

## -parameters

### -param pRect [in]

The rectangle to be invalidated, in client coordinates of the containing window. If this parameter is <b>NULL</b>, the object's full extent is invalidated.

### -param fErase [in]

Specifies whether the background within the update region is to be erased when the region is updated. If this parameter is <b>TRUE</b>, the background is erased. If this parameter is <b>FALSE</b>, the background remains unchanged.

## -returns

This method returns S_OK on success.

## -remarks

An object is only allowed to invalidate pixels contained in its own site rectangle. Any attempt to invalidate an area outside of that rectangle should result in a no-op.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>