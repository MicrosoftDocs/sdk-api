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

# IDirectWriterLock interface


## -description



			The 
<b>IDirectWriterLock</b> interface enables a single writer to obtain exclusive write access to a root storage object opened in direct mode while allowing concurrent access by multiple readers. This single-writer, multiple-reader mode does not require the overhead of making a snapshot copy of the storage for the readers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectWriterLock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectWriterLock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectWriterLock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8366b6b5-73c3-4b05-be68-c24ecd2eab96">HaveWriteAccess</a>
</td>
<td align="left" width="63%">
Indicates whether the write lock has been taken.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/849eeb79-60fd-4345-9e04-2ed7a7ede5ca">ReleaseWriteAccess</a>
</td>
<td align="left" width="63%">
Releases the write lock previously obtained.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4505bed-325b-494e-93bd-7bf23b3a1215">WaitForWriteAccess</a>
</td>
<td align="left" width="63%">
Obtains exclusive write access to a storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>



<a href="https://msdn.microsoft.com/3292484b-8eff-438d-b989-b58ae323872b">StgCreateDocfile</a>
 

 

