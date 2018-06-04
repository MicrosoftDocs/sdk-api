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

# IDataCollectorSet::put_RootPath


## -description


Retrieves or sets the base path where the subdirectories are created.
<div class="alert"><b>Warning</b>  If you change the <b>RootPath</b> property, you should change it to a directory that only contains performance logs. Setting this to another directory, such as the drive root or system root, may cause files to be inadvertently deleted when the logs are cleaned up by the system.</div><div> </div>This property is read/write.


## -parameters


## -remarks



If this property is changed from the default value, the specified directory must exist before the <a href="https://msdn.microsoft.com/63f0c7b7-0dc6-4491-a2f5-eaae9d22da61">IDataCollectorSet::Start</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/c0047144-5f99-4acd-ad96-054afcbe6eb9">IDataCollectorSet::LatestOutputLocation</a>



<a href="https://msdn.microsoft.com/d0ca2655-f65a-4bcb-8e9e-f247b4207e56">IDataCollectorSet::OutputLocation</a>



<a href="https://msdn.microsoft.com/c2c55fd9-3b29-46be-9792-acb095b1c0e4">IDataCollectorSet::Subdirectory</a>
 

 

