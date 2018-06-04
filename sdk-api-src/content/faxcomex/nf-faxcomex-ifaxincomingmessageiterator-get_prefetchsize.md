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

# IFaxIncomingMessageIterator::get_PrefetchSize


## -description


The <b>PrefetchSize</b> property indicates the size of the prefetch (read-ahead) buffer.

This property is read/write.


## -parameters


## -remarks



The prefetch buffer contains messages and makes the iteration process more efficient because you iterate through the buffer rather than through a folder. 

Changes you make to the size of the prefetch buffer take place immediately because <a href="https://msdn.microsoft.com/0969319b-7846-44a0-9667-161b326acea6">FaxIncomingMessageIterator</a> is a local object.

The value of the <i>lPrefetchSize</i> property determines how many fax messages the iterator object retrieves from the archive each time the object refreshes its contents. The default value is <a href="https://msdn.microsoft.com/447a730c-6033-46ab-9d90-0aad1aa4a429">lDEFAULT_PREFETCH_SIZE</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/f0b3071b-6936-4b19-873b-0ab28cfaea93">IFaxIncomingMessageIterator</a>



<a href="https://msdn.microsoft.com/0dc10f14-1ae3-47e5-aab2-53ddaa45b8a0">PrefetchSize</a>
 

 

