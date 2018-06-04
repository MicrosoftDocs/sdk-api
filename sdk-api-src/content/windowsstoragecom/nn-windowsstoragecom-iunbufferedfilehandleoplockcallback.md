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

# IUnbufferedFileHandleOplockCallback interface


## -description


Defines a callback method that you want to run when the opportunistic lock for a handle that you get by calling the <a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUnbufferedFileHandleOplockCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUnbufferedFileHandleOplockCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUnbufferedFileHandleOplockCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F5B6B4F6-61F2-4C5A-9E63-E9DC876FEB60">OnBrokenCallback</a>
</td>
<td align="left" width="63%">
Runs when the opportunistic lock for a handle that you get by calling the <a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a>
 

 

