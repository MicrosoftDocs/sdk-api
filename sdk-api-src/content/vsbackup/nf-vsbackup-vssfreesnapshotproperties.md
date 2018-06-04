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

# VssFreeSnapshotProperties function


## -description


The <b>VssFreeSnapshotProperties</b> function is 
    used to free the contents of a <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> 
    structure as part of managing its life cycle. The 
    <b>VSS_SNAPSHOT_PROP</b> structure is typically obtained by 
    using the 
    <a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a> method or the <a href="https://msdn.microsoft.com/59886344-d594-4eb8-9718-ab11a6627e8e">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a> method.

This function can also be used to initialize a 
    <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure before use or before 
    freeing the structure.
<div class="alert"><b>Note</b>  This function is exported as <b>VssFreeSnapshotPropertiesInternal</b>, but you should call <b>VssFreeSnapshotProperties</b>, not <b>VssFreeSnapshotPropertiesInternal</b>.</div><div> </div>

## -parameters




### -param pProp [in]

Pointer to a valid <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> 
      object.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a>



<a href="https://msdn.microsoft.com/59886344-d594-4eb8-9718-ab11a6627e8e">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a>



<a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>
 

 

