---
UID: NN:directmanipulation.IDirectManipulationContent
title: IDirectManipulationContent (directmanipulation.h)
author: windows-sdk-content
description: Encapsulates content inside a viewport, where content represents a visual surface clipped inside the viewport.
old-location: directmanipulation\idirectmanipulationcontent.htm
tech.root: directmanipulation
ms.assetid: 4d69a503-f998-4197-824f-4df48825c941
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectManipulationContent, IDirectManipulationContent interface [Direct Manipulation], IDirectManipulationContent interface [Direct Manipulation],described, directmanipulation.idirectmanipulationcontent, directmanipulation/IDirectManipulationContent
ms.topic: interface
f1_keywords: 
 - "directmanipulation/IDirectManipulationContent"
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - DirectManipulation.h
api_name:
 - IDirectManipulationContent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationContent interface


## -description


Encapsulates content inside a viewport, where content represents a visual surface clipped inside the viewport.

The content has a set of transforms that controls the visual movement of the surface during manipulation and inertia.
<div class="alert"><b>Note</b>  When implementing a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> object, ensure that the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedincrement">InterlockedIncrement</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockeddecrement">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationContent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationContent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationContent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-getcontentrect">GetContentRect</a>
</td>
<td align="left" width="63%">
Retrieves the bounding rectangle of the content, relative to the bounding rectangle of the viewport (if defined).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-getcontenttransform">GetContentTransform</a>
</td>
<td align="left" width="63%">
    Retrieves the transform applied to the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform">GetOutputTransform</a>
</td>
<td align="left" width="63%">
Gets the final transform applied to the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Retrieves the tag object set on this content. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-getviewport">GetViewport</a>
</td>
<td align="left" width="63%">
Retrieves the viewport that contains the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect">SetContentRect</a>
</td>
<td align="left" width="63%">
Specifies the bounding rectangle of the content, relative to its viewport.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-settag">SetTag</a>
</td>
<td align="left" width="63%">
Specifies the tag object for the content. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform">SyncContentTransform</a>
</td>
<td align="left" width="63%">
Modifies the content transform while maintaining the output transform.

</td>
</tr>
</table> 


## -remarks



The system provides an implementation of <b>IDirectManipulationContent</b>. 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
 

 

