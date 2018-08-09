---
UID: NF:ddpbackup.IDedupReadFileCallback.OrderContainersRestore
title: IDedupReadFileCallback::OrderContainersRestore
author: windows-sdk-content
description: This method provides the application with the ability to influence the order of the pending reads that are required to retrieve the target file.
old-location: dedup\idedupreadfilecallback_ordercontainersrestore.htm
old-project: dedup
ms.assetid: 25871056-5833-40DA-9C5B-690DCAB16E5C
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IDedupReadFileCallback interface [Data Deduplication API],OrderContainersRestore method, IDedupReadFileCallback.OrderContainersRestore, IDedupReadFileCallback::OrderContainersRestore, OrderContainersRestore, OrderContainersRestore method [Data Deduplication API], OrderContainersRestore method [Data Deduplication API],IDedupReadFileCallback interface, ddpbackup/IDedupReadFileCallback::OrderContainersRestore, dedup.idedupreadfilecallback_ordercontainersrestore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddpbackup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DEDUP_BACKUP_SUPPORT_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DdpBackup.h
api_name:
 - IDedupReadFileCallback.OrderContainersRestore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
      <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Possible return values 
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
 

 

