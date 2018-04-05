---
UID: NS:vss.__MIDL___MIDL_itf_vss_0000_0000_0001
title: "__MIDL___MIDL_itf_vss_0000_0000_0001"
author: windows-driver-content
description: A union of VSS_SNAPSHOT_PROP and VSS_PROVIDER_PROP structures, which is used by the VSS_OBJECT_PROP structure.
old-location: base\vss_object_union.htm
old-project: VSS
ms.assetid: e8d70f20-00a9-4cae-a92c-e3f3673a8db3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: VSS_OBJECT_UNION, VSS_OBJECT_UNION union [VSS], __MIDL___MIDL_itf_vss_0000_0000_0001, _win32_vss_object_union, base.vss_object_union, vss/VSS_OBJECT_UNION
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
req.typenames: VSS_OBJECT_UNION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vss.h
api_name:
-	VSS_OBJECT_UNION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# __MIDL___MIDL_itf_vss_0000_0000_0001 structure


## -description


The <b>VSS_OBJECT_UNION</b> structure is a union 
    of <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> and 
    <a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a> structures, which is used by the 
    <a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structure to hold information 
    about a specific shadow copy or provider.


## -struct-fields




### -field Snap

Information about a specific shadow copy. For more information, see 
      <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>.


### -field Prov

Information about a specific provider. For more information, see 
      <a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a>.


## -remarks



The <b>VSS_OBJECT_UNION</b> structure is used only as a 
    member of the <a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> 
    structure.

Applications need to consult the <b>Type</b> member of 
    <a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> to determine whether the 
    <b>VSS_OBJECT_UNION</b> contains a 
    <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> or 
    <a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a> object.

When a <a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structure has been returned 
    by a member method of a COM interface (from, for example, 
    <a href="https://msdn.microsoft.com/9bfaba94-802f-47f5-9843-acc05b32f1b2">IVssEnumObject:Next</a>), an application must call 
    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> for every string and byte array value 
    contained in its constituent structure (either 
    <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> or 
    <a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a>).

In the case of <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>, this can be done 
    manually, or the utility function 
    <a href="https://msdn.microsoft.com/d5b5883b-03d5-4a83-af2e-f4d22e26ee82">VssFreeSnapshotProperties</a> can be used.




## -see-also




<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a>



<a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a>



<a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>
 

 

