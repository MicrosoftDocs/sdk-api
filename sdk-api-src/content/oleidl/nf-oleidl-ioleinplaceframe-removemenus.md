---
UID: NF:oleidl.IOleInPlaceFrame.RemoveMenus
title: IOleInPlaceFrame::RemoveMenus (oleidl.h)
description: Removes a container's menu elements from the composite menu.
helpviewer_keywords: ["IOleInPlaceFrame interface [COM]","RemoveMenus method","IOleInPlaceFrame.RemoveMenus","IOleInPlaceFrame::RemoveMenus","RemoveMenus","RemoveMenus method [COM]","RemoveMenus method [COM]","IOleInPlaceFrame interface","_ole_ioleinplaceframe_removemenus","com.ioleinplaceframe_removemenus","oleidl/IOleInPlaceFrame::RemoveMenus"]
old-location: com\ioleinplaceframe_removemenus.htm
tech.root: com
ms.assetid: 92d9fcda-8ede-4f38-ad56-59c4a75fe45a
ms.date: 12/05/2018
ms.keywords: IOleInPlaceFrame interface [COM],RemoveMenus method, IOleInPlaceFrame.RemoveMenus, IOleInPlaceFrame::RemoveMenus, RemoveMenus, RemoveMenus method [COM], RemoveMenus method [COM],IOleInPlaceFrame interface, _ole_ioleinplaceframe_removemenus, com.ioleinplaceframe_removemenus, oleidl/IOleInPlaceFrame::RemoveMenus
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
 - IOleInPlaceFrame::RemoveMenus
 - oleidl/IOleInPlaceFrame::RemoveMenus
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
 - IOleInPlaceFrame.RemoveMenus
---

# IOleInPlaceFrame::RemoveMenus


## -description

Removes a container's menu elements from the composite menu.

## -parameters

### -param hmenuShared [in]

A handle to the in-place composite menu that was constructed by calls to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-insertmenus">IOleInPlaceFrame::InsertMenus</a> and the <a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a> function.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>

## -remarks

The object should always give the container a chance to remove its menu elements from the composite menu before deactivating the shared user interface.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method is called by the object application while it is being UI-deactivated to remove its menus.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceframe">IOleInPlaceFrame</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-setmenu">IOleInPlaceFrame::SetMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a>