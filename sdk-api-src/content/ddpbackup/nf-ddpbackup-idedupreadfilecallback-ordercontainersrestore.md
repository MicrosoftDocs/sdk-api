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

# IDedupReadFileCallback::OrderContainersRestore


## -description


This method provides the application with the ability to influence the order of the pending reads that 
    are required to retrieve the target file.

Given a list of container files that hold data for the 
    restore target file, generates a list of container file extents in a sorted order that results in an efficient 
    cross-container read plan from the backup store.

Implementation of this method by the application is 
    optional.


## -parameters




### -param NumberOfContainers [in]

Number of container paths in the <i>ContainerPaths</i> array.


### -param ContainerPaths [in]

Array of paths to container files that must be read in order to restore the file specified in the 
      <a href="dedup.idedupbackupsupport_restorefile">IDedupBackupSupport::RestoreFiles</a> 
      call. Each element is a full path from the root directory of the volume to a container file.


### -param ReadPlanEntries [out]

Pointer to a ULONG variable that receives the number of 
      <a href="https://msdn.microsoft.com/D7CEC0C4-0472-467C-87F1-1496C9F08296">DEDUP_CONTAINER_EXTENT</a> structures in the array 
      that the <i>ReadPlan</i> parameter points to.


### -param ReadPlan [out]

Pointer to a buffer that receives an array of 
      <a href="https://msdn.microsoft.com/D7CEC0C4-0472-467C-87F1-1496C9F08296">DEDUP_CONTAINER_EXTENT</a> structures.


## -returns



This method can return standard <b>HRESULT</b> values, such as 
      <b>S_OK</b>. It can also return converted 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a> using the 
      <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Possible return values 
      include the following.




## -remarks



Given a list of container files that hold data for the restore target file, the application optionally 
    generates a list of container store file extents in a sorted order that results in an efficient cross-container 
    read plan. For a backup store located on tape, this would normally be in tape order.

In the case where a container is stored in multiple extents in the backup store—for 
    example, as a result of an incremental backup sequence—the application may also return 
    multiple container extents for each logical container file.

The application may return 
    <b>S_OK</b> and <b>NULL</b> output parameters to skip the read plan 
    optimizations. In this case, container read order will be chosen by Data Deduplication.




## -see-also




<a href="https://msdn.microsoft.com/D7CEC0C4-0472-467C-87F1-1496C9F08296">DEDUP_CONTAINER_EXTENT</a>



<a href="https://msdn.microsoft.com/0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C">IDedupReadFileCallback</a>
 

 

