---
UID: NS:vss._VSS_OBJECT_PROP
title: "_VSS_OBJECT_PROP"
author: windows-sdk-content
description: Defines the properties of a provider, volume, shadow copy, or shadow copy set.
old-location: base\vss_object_prop.htm
tech.root: VSS
ms.assetid: 90664042-e9a0-4959-a975-9289477d2394
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PVSS_OBJECT_PROP, PVSS_OBJECT_PROP, PVSS_OBJECT_PROP structure pointer [VSS], VSS_OBJECT_PROP, VSS_OBJECT_PROP structure [VSS], _VSS_OBJECT_PROP, _win32_vss_object_prop, base.vss_object_prop, vss/PVSS_OBJECT_PROP, vss/VSS_OBJECT_PROP"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_OBJECT_PROP
product: Windows
targetos: Windows
req.typenames: VSS_OBJECT_PROP, *PVSS_OBJECT_PROP
req.redist: 
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
 

 

