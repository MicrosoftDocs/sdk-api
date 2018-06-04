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

# _UMS_SYSTEM_THREAD_INFORMATION structure


## -description


Specifies a UMS scheduler thread, UMS worker thread, or non-UMS thread. The <a href="https://msdn.microsoft.com/7c8347b6-6546-4ea9-9b2a-11794782f482">GetUmsSystemThreadInformation</a> function uses this structure. 


## -struct-fields




### -field UmsVersion

The UMS version. This member must be UMS_VERSION.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.IsUmsSchedulerThread

A bitfield that specifies a UMS scheduler thread. If <b>IsUmsSchedulerThread</b> is set, <b>IsUmsWorkerThread</b> must be clear. 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.IsUmsWorkerThread

A bitfield that specifies a UMS worker thread. If <b>IsUmsWorkerThread</b>  is set, <b>IsUmsSchedulerThread</b> must be clear. 


### -field DUMMYUNIONNAME.ThreadUmsFlags

 




## -remarks



If both <b>IsUmsSchedulerThread</b>  and <b>IsUmsWorkerThread</b> are clear, the structure specifies a non-UMS thread. 



