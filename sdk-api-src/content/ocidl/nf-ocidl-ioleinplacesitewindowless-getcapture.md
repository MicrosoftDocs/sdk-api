---
UID: NF:ocidl.IOleInPlaceSiteWindowless.GetCapture
title: IOleInPlaceSiteWindowless::GetCapture (ocidl.h)
description: Called by an in-place active, windowless object to determine whether it still has the mouse capture.
helpviewer_keywords: ["GetCapture","GetCapture method [COM]","GetCapture method [COM]","IOleInPlaceSiteWindowless interface","IOleInPlaceSiteWindowless interface [COM]","GetCapture method","IOleInPlaceSiteWindowless.GetCapture","IOleInPlaceSiteWindowless::GetCapture","_ole_ioleinplacesitewindowless_getcapture","com.ioleinplacesitewindowless_getcapture","ocidl/IOleInPlaceSiteWindowless::GetCapture"]
old-location: com\ioleinplacesitewindowless_getcapture.htm
tech.root: com
ms.assetid: adbe9c66-d716-4489-b705-43a5317c7646
ms.date: 12/05/2018
ms.keywords: GetCapture, GetCapture method [COM], GetCapture method [COM],IOleInPlaceSiteWindowless interface, IOleInPlaceSiteWindowless interface [COM],GetCapture method, IOleInPlaceSiteWindowless.GetCapture, IOleInPlaceSiteWindowless::GetCapture, _ole_ioleinplacesitewindowless_getcapture, com.ioleinplacesitewindowless_getcapture, ocidl/IOleInPlaceSiteWindowless::GetCapture
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
 - IOleInPlaceSiteWindowless::GetCapture
 - ocidl/IOleInPlaceSiteWindowless::GetCapture
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
 - IOleInPlaceSiteWindowless.GetCapture
---

# IOleInPlaceSiteWindowless::GetCapture


## -description

Called by an in-place active, windowless object to determine whether it still has the mouse capture.



## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object does not currently have the mouse capture.

</td>
</tr>
</table>

## -remarks

As an alternative to calling this method, the object can cache information about whether it has the mouse capture.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>
