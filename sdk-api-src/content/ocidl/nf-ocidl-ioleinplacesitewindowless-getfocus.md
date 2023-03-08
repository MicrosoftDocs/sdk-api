---
UID: NF:ocidl.IOleInPlaceSiteWindowless.GetFocus
title: IOleInPlaceSiteWindowless::GetFocus (ocidl.h)
description: Called by an in-place active, windowless object to determine whether it still has the keyboard focus.
helpviewer_keywords: ["GetFocus","GetFocus method [COM]","GetFocus method [COM]","IOleInPlaceSiteWindowless interface","IOleInPlaceSiteWindowless interface [COM]","GetFocus method","IOleInPlaceSiteWindowless.GetFocus","IOleInPlaceSiteWindowless::GetFocus","_ole_ioleinplacesitewindowless_getfocus","com.ioleinplacesitewindowless_getfocus","ocidl/IOleInPlaceSiteWindowless::GetFocus"]
old-location: com\ioleinplacesitewindowless_getfocus.htm
tech.root: com
ms.assetid: 282f350c-d196-40c2-880f-55f28dc48f2b
ms.date: 12/05/2018
ms.keywords: GetFocus, GetFocus method [COM], GetFocus method [COM],IOleInPlaceSiteWindowless interface, IOleInPlaceSiteWindowless interface [COM],GetFocus method, IOleInPlaceSiteWindowless.GetFocus, IOleInPlaceSiteWindowless::GetFocus, _ole_ioleinplacesitewindowless_getfocus, com.ioleinplacesitewindowless_getfocus, ocidl/IOleInPlaceSiteWindowless::GetFocus
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
 - IOleInPlaceSiteWindowless::GetFocus
 - ocidl/IOleInPlaceSiteWindowless::GetFocus
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
 - IOleInPlaceSiteWindowless.GetFocus
---

# IOleInPlaceSiteWindowless::GetFocus


## -description

Called by an in-place active, windowless object to determine whether it still has the keyboard focus.



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
The object does not currently have the keyboard focus.

</td>
</tr>
</table>

## -remarks

A windowless object calls this method to find out if it currently has the focus or not. As an alternative to calling this method, the object can cache information about whether it has the keyboard focus or not.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>
