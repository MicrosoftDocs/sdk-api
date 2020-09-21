---
UID: NF:ocidl.IOleInPlaceSiteWindowless.ReleaseDC
title: IOleInPlaceSiteWindowless::ReleaseDC (ocidl.h)
description: Releases the device context previously obtained by a call to IOleInPlaceSiteWindowless::GetDC.
helpviewer_keywords: ["IOleInPlaceSiteWindowless interface [COM]","ReleaseDC method","IOleInPlaceSiteWindowless.ReleaseDC","IOleInPlaceSiteWindowless::ReleaseDC","ReleaseDC","ReleaseDC method [COM]","ReleaseDC method [COM]","IOleInPlaceSiteWindowless interface","_ole_ioleinplacesitewindowless_releasedc","com.ioleinplacesitewindowless_releasedc","ocidl/IOleInPlaceSiteWindowless::ReleaseDC"]
old-location: com\ioleinplacesitewindowless_releasedc.htm
tech.root: com
ms.assetid: 8778a58c-2995-4c14-826c-9c97e97e957b
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSiteWindowless interface [COM],ReleaseDC method, IOleInPlaceSiteWindowless.ReleaseDC, IOleInPlaceSiteWindowless::ReleaseDC, ReleaseDC, ReleaseDC method [COM], ReleaseDC method [COM],IOleInPlaceSiteWindowless interface, _ole_ioleinplacesitewindowless_releasedc, com.ioleinplacesitewindowless_releasedc, ocidl/IOleInPlaceSiteWindowless::ReleaseDC
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
 - IOleInPlaceSiteWindowless::ReleaseDC
 - ocidl/IOleInPlaceSiteWindowless::ReleaseDC
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
 - IOleInPlaceSiteWindowless.ReleaseDC
---

# IOleInPlaceSiteWindowless::ReleaseDC


## -description

Releases the device context previously obtained by a call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-getdc">IOleInPlaceSiteWindowless::GetDC</a>.

## -parameters

### -param hDC [in]

The device context to be released.

## -returns

This method returns S_OK on success.

## -remarks

An object calls this method to notify its container that the object is done with the device context. If the device context was used for drawing, the container should ensure that all overlapping objects are repainted correctly. If the device context was an offscreen device context, its content should also be copied to the screen in the rectangle originally passed to <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-getdc">IOleInPlaceSiteWindowless::GetDC</a>. See <b>IOleInPlaceSiteWindowless::GetDC</b> for implementation notes relevant to <b>IOleInPlaceSiteWindowless::ReleaseDC</b>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleinplacesitewindowless-getdc">IOleInPlaceSiteWindowless::GetDC</a>