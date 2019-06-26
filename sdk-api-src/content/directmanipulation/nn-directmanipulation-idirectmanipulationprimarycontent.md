---
UID: NN:directmanipulation.IDirectManipulationPrimaryContent
title: IDirectManipulationPrimaryContent (directmanipulation.h)
author: windows-sdk-content
description: Encapsulates the primary content inside a viewport.
old-location: directmanipulation\idirectmanipulationprimarycontent.htm
tech.root: directmanipulation
ms.assetid: 9910F5F5-950F-4099-9808-B46FA5BBA6FB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectManipulationPrimaryContent, IDirectManipulationPrimaryContent interface [Direct Manipulation], IDirectManipulationPrimaryContent interface [Direct Manipulation],described, directmanipulation.idirectmanipulationprimarycontent, directmanipulation/IDirectManipulationPrimaryContent
ms.topic: interface
f1_keywords: 
 - "directmanipulation/IDirectManipulationPrimaryContent"
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
 - IDirectManipulationPrimaryContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationPrimaryContent interface


## -description


Encapsulates the primary content inside a viewport. Primary content is the content specified during the creation of a viewport.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationPrimaryContent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationPrimaryContent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationPrimaryContent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-getcenterpoint">GetCenterPoint</a>
</td>
<td align="left" width="63%">
    Retrieves the center point of the manipulation in content coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-getinertiaendtransform">GetInertiaEndTransform</a>
</td>
<td align="left" width="63%">
Gets the final transform, including inertia, of the primary content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-sethorizontalalignment">SetHorizontalAlignment</a>
</td>
<td align="left" width="63%">
Sets the horizontal alignment of the primary content relative to the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate">SetSnapCoordinate</a>
</td>
<td align="left" width="63%">
    Specifies the coordinate system for snap points or snap intervals. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval">SetSnapInterval</a>
</td>
<td align="left" width="63%">
    Specifies snap points for the inertia end position at uniform intervals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints">SetSnapPoints</a>
</td>
<td align="left" width="63%">
Specifies the snap points for the inertia rest position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnaptype">SetSnapType</a>
</td>
<td align="left" width="63%">
Specifies the type of snap point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setverticalalignment">SetVerticalAlignment</a>
</td>
<td align="left" width="63%">
Specifies the vertical alignment of the primary content in the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setzoomboundaries">SetZoomBoundaries</a>
</td>
<td align="left" width="63%">
Specifies the minimum and maximum boundaries for zoom.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
 

 

