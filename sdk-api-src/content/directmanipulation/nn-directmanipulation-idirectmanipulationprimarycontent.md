---
UID: NN:directmanipulation.IDirectManipulationPrimaryContent
title: IDirectManipulationPrimaryContent
author: windows-sdk-content
description: Encapsulates the primary content inside a viewport.
old-location: directmanipulation\idirectmanipulationprimarycontent.htm
old-project: directmanipulation
ms.assetid: 9910F5F5-950F-4099-9808-B46FA5BBA6FB
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationPrimaryContent, IDirectManipulationPrimaryContent interface [Direct Manipulation], IDirectManipulationPrimaryContent interface [Direct Manipulation],described, directmanipulation.idirectmanipulationprimarycontent, directmanipulation/IDirectManipulationPrimaryContent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
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
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationPrimaryContent interface


## -description


Encapsulates the primary content inside a viewport. Primary content is the content specified during the creation of a viewport.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationPrimaryContent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationPrimaryContent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e38c1445-af4b-463b-8796-d72d69cb19c6">GetCenterPoint</a>
</td>
<td align="left" width="63%">
    Retrieves the center point of the manipulation in content coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BCF0E48F-C47E-42BE-90F8-25737301DC9C">GetInertiaEndTransform</a>
</td>
<td align="left" width="63%">
Gets the final transform, including inertia, of the primary content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94716ec8-325e-4e9e-9a30-1d9999bdb9c3">SetHorizontalAlignment</a>
</td>
<td align="left" width="63%">
Sets the horizontal alignment of the primary content relative to the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f9afe1b-20f4-45fa-a63b-25b7a0c597af">SetSnapCoordinate</a>
</td>
<td align="left" width="63%">
    Specifies the coordinate system for snap points or snap intervals. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99d039fe-017a-47c5-95a1-5000efe92ba0">SetSnapInterval</a>
</td>
<td align="left" width="63%">
    Specifies snap points for the inertia end position at uniform intervals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3257952d-903b-455c-9422-9739411a5924">SetSnapPoints</a>
</td>
<td align="left" width="63%">
Specifies the snap points for the inertia rest position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f1ad54d-8c9a-4b3c-a78b-fe02cb889ca9">SetSnapType</a>
</td>
<td align="left" width="63%">
Specifies the type of snap point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/111f0358-0955-4ebb-b273-c17d3fb84d75">SetVerticalAlignment</a>
</td>
<td align="left" width="63%">
Specifies the vertical alignment of the primary content in the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77e4054b-637f-4cff-bfab-0e2a0e992c59">SetZoomBoundaries</a>
</td>
<td align="left" width="63%">
Specifies the minimum and maximum boundaries for zoom.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

