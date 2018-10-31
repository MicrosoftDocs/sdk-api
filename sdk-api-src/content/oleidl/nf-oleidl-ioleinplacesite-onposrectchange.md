---
UID: NF:oleidl.IOleInPlaceSite.OnPosRectChange
title: IOleInPlaceSite::OnPosRectChange
author: windows-sdk-content
description: Notifies the container that the object extents have changed.
old-location: com\ioleinplacesite_onposrectchange.htm
tech.root: com
ms.assetid: a12d6a2a-6581-41e3-b33d-74af5d772e71
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IOleInPlaceSite interface [COM],OnPosRectChange method, IOleInPlaceSite.OnPosRectChange, IOleInPlaceSite::OnPosRectChange, IOleInPlaceSiteWindowless.OnPosRectChange, OnPosRectChange, OnPosRectChange method [COM], OnPosRectChange method [COM],IOleInPlaceSite interface, _ole_ioleinplacesite_onposrectchange, com.ioleinplacesite_onposrectchange, oleidl/IOleInPlaceSite::OnPosRectChange
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
 - browsewm.dll
api_name:
 - IOleInPlaceSite.OnPosRectChange
 - IOleInPlaceSiteWindowless.OnPosRectChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceSite::OnPosRectChange


## -description


Notifies the container that the object extents have changed.


## -parameters




### -param lprcPosRect [in]

A pointer a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the position of the in-place object in the client coordinates of its parent window.


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
The supplied pointer is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The <b>OnPosRectChange</b> method is called by the in-place object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
When the in-place object calls <b>OnPosRectChange</b>, the container must call <a href="https://msdn.microsoft.com/5ae2e44b-d2e2-4351-b4fa-8c37419a2bcb">IOleInPlaceObject::SetObjectRects</a> to specify the new position of the in-place window and the clipping rectangle. Only then does the object resize its window.

In most cases, the object grows to the right and/or down. There could be cases where the object grows to the left and/or up, as conveyed through <i>lprcPosRect</i>. It is also possible to change the object's position without changing its size.




## -see-also




<a href="https://msdn.microsoft.com/5ae2e44b-d2e2-4351-b4fa-8c37419a2bcb">IOleInPlaceObject::SetObjectRects</a>



<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>
 

 

