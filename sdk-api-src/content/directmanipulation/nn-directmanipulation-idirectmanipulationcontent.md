---
UID: NN:directmanipulation.IDirectManipulationContent
title: IDirectManipulationContent
author: windows-sdk-content
description: Encapsulates content inside a viewport, where content represents a visual surface clipped inside the viewport.
old-location: directmanipulation\idirectmanipulationcontent.htm
tech.root: directmanipulation
ms.assetid: 4d69a503-f998-4197-824f-4df48825c941
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDirectManipulationContent, IDirectManipulationContent interface [Direct Manipulation], IDirectManipulationContent interface [Direct Manipulation],described, directmanipulation.idirectmanipulationcontent, directmanipulation/IDirectManipulationContent
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationContent interface


## -description


Encapsulates content inside a viewport, where content represents a visual surface clipped inside the viewport.

The content has a set of transforms that controls the visual movement of the surface during manipulation and inertia.
<div class="alert"><b>Note</b>  When implementing a <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> object, ensure that the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="https://msdn.microsoft.com/87eda7fb-966d-4630-9da6-8933b53daadd">InterlockedIncrement</a> and <a href="https://msdn.microsoft.com/d6ed6cb1-aa10-48f4-9b62-73708ff4d1e3">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationContent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationContent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/26a5736e-633e-4451-a339-c5f88913bcf6">GetContentRect</a>
</td>
<td align="left" width="63%">
Retrieves the bounding rectangle of the content, relative to the bounding rectangle of the viewport (if defined).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9db4f521-227c-4e2f-8c7d-44ae4a25651e">GetContentTransform</a>
</td>
<td align="left" width="63%">
    Retrieves the transform applied to the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8f746a4-650f-4f6d-8734-2e98f01898f2">GetOutputTransform</a>
</td>
<td align="left" width="63%">
Gets the final transform applied to the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11acda14-3932-43e4-b45e-e129886c354f">GetTag</a>
</td>
<td align="left" width="63%">
Retrieves the tag object set on this content. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b03545d2-73a4-4638-818a-34f5957408e4">GetViewport</a>
</td>
<td align="left" width="63%">
Retrieves the viewport that contains the content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41b14e56-ba24-4ad2-9dac-28daf7d13c6a">SetContentRect</a>
</td>
<td align="left" width="63%">
Specifies the bounding rectangle of the content, relative to its viewport.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0dce3dd-3fbf-41ea-ba70-8574701d101e">SetTag</a>
</td>
<td align="left" width="63%">
Specifies the tag object for the content. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e70b208-05b5-4b84-a582-fd835acdd777">SyncContentTransform</a>
</td>
<td align="left" width="63%">
Modifies the content transform while maintaining the output transform.

</td>
</tr>
</table> 


## -remarks



The system provides an implementation of <b>IDirectManipulationContent</b>. 




## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

