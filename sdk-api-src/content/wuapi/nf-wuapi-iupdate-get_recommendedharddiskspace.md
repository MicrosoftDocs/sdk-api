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

# IUpdate::get_RecommendedHardDiskSpace


## -description


Gets the recommended free space that should be available on the hard disk before you install the update. The free space is specified in megabytes (MB).

This property is read-only.


## -parameters


## -remarks



The following properties of the <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface return 0 (zero) when the information is not available:

<ul>
<li>
<a href="https://msdn.microsoft.com/21003be2-c14e-48d4-a51f-ed75b1b47284">RecommendedCpuSpeed</a>
</li>
<li><b>RecommendedHardDiskSpace</b></li>
<li>
<a href="https://msdn.microsoft.com/68a8341b-ba0a-4694-89c3-34fefb950bf7">RecommendedMemory</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

