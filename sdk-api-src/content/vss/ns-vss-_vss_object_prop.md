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

# _VSS_OBJECT_PROP structure


## -description


The <b>VSS_OBJECT_PROP</b> structure defines the 
    properties of a provider, volume, shadow copy, or shadow copy set.


## -struct-fields




### -field Type

Object type. Refer to <a href="https://msdn.microsoft.com/b7c91003-0ce7-463e-a816-c212da9dc31e">VSS_OBJECT_TYPE</a>.


### -field Obj

Object properties: a union of <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> 
      and <a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a> structures. (See 
      <a href="https://msdn.microsoft.com/e8d70f20-00a9-4cae-a92c-e3f3673a8db3">VSS_OBJECT_UNION</a>.) 
     

It contains information for an object of the type specified by the <b>Type</b> member of 
      the <b>VSS_OBJECT_PROP</b> structure. Objects can be 
      providers, volumes, shadow copies, or shadow copy sets.


## -remarks



A requester obtains <b>VSS_OBJECT_PROP</b> structures by 
    using <a href="https://msdn.microsoft.com/9bfaba94-802f-47f5-9843-acc05b32f1b2">IVssEnumObject::Next</a> to iterate over the list 
    of objects returned by a call to 
    <a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a>.

As its members are filled by a COM interface, prior to deleting the property structures 
    <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> and 
    <a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a>, the memory they contain must be 
    released by calling <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> for every string and 
    byte array value contained in each structure.

In the case of <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>, this can be done 
    manually, or the utility function 
    <a href="https://msdn.microsoft.com/d5b5883b-03d5-4a83-af2e-f4d22e26ee82">VssFreeSnapshotProperties</a> can be used.




## -see-also




<a href="https://msdn.microsoft.com/b7c91003-0ce7-463e-a816-c212da9dc31e">VSS_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/e8d70f20-00a9-4cae-a92c-e3f3673a8db3">VSS_OBJECT_UNION</a>



<a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a>



<a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>
 

 

