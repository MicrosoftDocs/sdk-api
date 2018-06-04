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

# IMFASFStreamPrioritization interface


## -description


<div class="alert"><b>Note</b>  This interface is not implemented.</div><div> </div>Manages information about the relative priorities of a group of streams in an Advanced Systems Format (ASF) profile. This interface manages information about the relative priorities of a group of streams in an ASF profile. Priority is used in streaming to determine which streams should be dropped first when available bandwidth decreases.

The ASF stream prioritization object exposes this interface. The stream prioritization object maintains a list of stream numbers in priority order. The methods of this interface manipulate and interrogate that list. To obtain a pointer to this interface, call the <a href="https://msdn.microsoft.com/1c3a5470-eba9-4233-8744-8630002d3fa0">IMFASFProfile::CreateStreamPrioritization</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFStreamPrioritization</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFASFStreamPrioritization</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFStreamPrioritization</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/440d2838-0314-45f7-b73b-653fe5535c88">AddStream</a>
</td>
<td align="left" width="63%">

          Adds a stream to the stream priority list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">

          Creates a copy of the stream prioritization object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/460a929b-71bf-4f41-9e7a-af04a8f1c10f">GetStream</a>
</td>
<td align="left" width="63%">

          Retrieves the stream number of a stream in the stream priority list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c9dacbb-a952-411e-82df-0c8768d0b3fe">GetStreamCount</a>
</td>
<td align="left" width="63%">

          Retrieves the number of entries in the stream priority list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6139042-9c78-4fe7-8549-655e35be2862">RemoveStream</a>
</td>
<td align="left" width="63%">

          Removes a stream from the stream priority list.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

