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

# IFsrmFileManagementJob::get_OperationType


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The type of file management job. The type determines the operation to perform on a file when all 
    conditions are met.

This property is read/write.


## -parameters


## -remarks



If the type is <b>FsrmFileManagementType_Expiration</b>, FSRM moves the files that meet 
    all the file management job's conditions to the path specified by the 
    <a href="https://msdn.microsoft.com/7c8a2584-23ff-4839-b426-8f5411955746">ExpirationDirectory</a> property 
    when the job is run.

If the type is <b>FsrmFileManagementType_Custom</b>, FSRM executes the custom action 
    specified in the <a href="https://msdn.microsoft.com/25014b2d-4f08-45bb-a4c4-d8ab72dc53b1">CustomAction</a> 
    property for every file that meets all the file management job's conditions when the file management job is 
    run.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

