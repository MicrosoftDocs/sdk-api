---
UID: NN:textstor.IAnchor
title: IAnchor
author: windows-sdk-content
description: The IAnchor interface is implemented by the TSF manager. Clients of Microsoft Active Accessibility use IAnchor anchor objects to delimit a range of text within a text stream.
old-location: tsf\ianchor.htm
tech.root: TSF
ms.assetid: a7d52959-8386-464f-958d-c870f286b265
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IAnchor, IAnchor interface [Text Services Framework], IAnchor interface [Text Services Framework],described, textstor/IAnchor, tsf.ianchor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IAnchor
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IAnchor interface


## -description


The <b>IAnchor</b> interface is implemented by the TSF manager. Clients of <a href="https://msdn.microsoft.com/en-us/library/ms971350(v=MSDN.10).aspx">Microsoft Active Accessibility</a> use <b>IAnchor</b> anchor objects to delimit a range of text within a text stream.

The interface ID is IID_IAnchor.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnchor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAnchor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnchor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3780ab3d-6b77-45bc-9630-747fa5caaecc">ClearChangeHistory</a>
</td>
<td align="left" width="63%">
Clears the change history flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c5e767a-5f66-4ecf-89f1-b27ed38e887b">Clone</a>
</td>
<td align="left" width="63%">
Produces a new anchor object positioned at the same location, and with the same gravity, as the current anchor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/227ed0c0-0bdd-49af-b5dc-fdb69913b9c1">Compare</a>
</td>
<td align="left" width="63%">
Compares the relative position of two anchors within a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d373a379-1d27-4438-abaf-2e11f2332790">GetChangeHistory</a>
</td>
<td align="left" width="63%">
Gets the change history of deletions that have occurred immediately preceding or following the anchor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c56a4c25-ac43-4fd3-8d6b-943eb0233ed4">GetGravity</a>
</td>
<td align="left" width="63%">
Retrieves the gravity of the anchor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2dedce7-f64d-406a-bebc-9a4b51a1ae38">IsEqual</a>
</td>
<td align="left" width="63%">
Specifies the equality or inequality of the positions of two anchors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6be9a29-5d39-4719-a7e3-0c0921ecd89a">SetChangeHistoryMask</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c532abcf-9ae0-4566-80f7-0bb4ae908fce">SetGravity</a>
</td>
<td align="left" width="63%">
Sets the gravity of the anchor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e57a78e6-42e6-4a2b-b4e1-20bb64add872">Shift</a>
</td>
<td align="left" width="63%">
Shifts the anchor forward or backward.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f24f0155-fab6-46fb-9bff-598cd25e17ea">ShiftRegion</a>
</td>
<td align="left" width="63%">
Shifts the anchor into an adjacent region in the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0fb9a08-3f46-4d2f-8887-e80dc0bade1b">ShiftTo</a>
</td>
<td align="left" width="63%">
Shifts the current anchor to the same position as another anchor.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/ms971350(v=MSDN.10).aspx">Microsoft Active Accessibility</a>
 

 

