---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOleDocument interface


## -description


Enables a document object to communicate to containers its ability to create views of its data. This interface also enables a document object to enumerate its views and to provide containers with miscellaneous information about itself, such as whether it supports multiple views or complex rectangles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleDocument</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IOleDocument</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleDocument</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/709d7ff4-d32d-405f-8839-b05df49ef751">CreateView</a>
</td>
<td align="left" width="63%">
Creates a document view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca186853-0792-4a34-b718-46927a73e670">EnumViews</a>
</td>
<td align="left" width="63%">
Creates an object that enumerates the views supported by a document object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de279d46-057e-4c3a-8af3-14f7b65147fd">GetDocMiscStatus</a>
</td>
<td align="left" width="63%">
Retrieves status information about the document object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5c8b455e-7740-4f71-aef6-27390a11a1a3">IOleCommandTarget</a>



<a href="https://msdn.microsoft.com/cac435c9-caee-4751-9ad8-df48b6d4c7e0">IOleDocumentSite</a>



<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/eb0d15c0-8a34-4211-b840-29d5862cf767">IPrint</a>
 

 

