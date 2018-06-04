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

# IDataManager::get_MaxSize


## -description


Retrieves or sets the maximum disk space to be used by all data collectors in the set. 

This property is read/write.


## -parameters


## -remarks



The maximum value applies to all files in all subfolders under the path specified by the <a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">IDataCollectorSet::RootPath</a> property. 

This value is used by the data manager:

<ul>
<li>Before the data collector set starts if the value of the <a href="https://msdn.microsoft.com/23c7aced-d159-4d5e-a9ff-f0ca5b3e4470">IDataManager::CheckBeforeRunning</a> property is VARIANT_TRUE. If the maximum size is exceeded, the manager prevents the data collector set from running.</li>
<li>After the collection is completed. If the maximum size is exceeded, the data manager will start deleting folders (according to the <a href="https://msdn.microsoft.com/541cd28c-2e01-4b8a-9cd3-044896c8fb80">IDataManager::ResourcePolicy</a> property) until the total size is below the maximum size.</li>
</ul>
The maximum size value is ignored for performance counter log collection. To work around this issue, you can do one of two things:

<ul>
<li>Set the <a href="https://msdn.microsoft.com/d1b35b02-cfda-42a4-bd1d-d837a91861d6">IDataCollector::LogCircular</a> property to <b>True</b> and set the <a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">IDataCollectorSet::SegmentMaxSize</a> property to the desired maximum size.</li>
<li>Set the <a href="https://msdn.microsoft.com/d1b35b02-cfda-42a4-bd1d-d837a91861d6">IDataCollector::LogCircular</a> property to <b>False</b>, set the <a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">IDataCollectorSet::SegmentMaxSize</a> property equal to the maximum folder size, and set the <a href="https://msdn.microsoft.com/5ecac3dd-0cd1-4563-a6b3-1b98e29fe769">IDataCollectorSet::Segment</a> property to <b>False</b>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>
 

 

