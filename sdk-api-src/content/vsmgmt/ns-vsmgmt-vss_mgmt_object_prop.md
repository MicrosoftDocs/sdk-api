---
UID: NS:vsmgmt._VSS_MGMT_OBJECT_PROP
title: VSS_MGMT_OBJECT_PROP (vsmgmt.h)
author: windows-sdk-content
description: Defines the properties of a volume, shadow copy storage volume, or a shadow copy storage area.
old-location: base\vss_mgmt_object_prop.htm
tech.root: VSS
ms.assetid: 86681207-969e-4b33-aff8-79454ab04829
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PVSS_MGMT_OBJECT_PROP, PVSS_MGMT_OBJECT_PROP, PVSS_MGMT_OBJECT_PROP structure pointer [VSS], VSS_MGMT_OBJECT_PROP, VSS_MGMT_OBJECT_PROP structure [VSS], base.vss_mgmt_object_prop, vsmgmt/PVSS_MGMT_OBJECT_PROP, vsmgmt/VSS_MGMT_OBJECT_PROP"
ms.topic: struct
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - VsMgmt.h
api_name:
 - VSS_MGMT_OBJECT_PROP
product: Windows
targetos: Windows
req.typenames: VSS_MGMT_OBJECT_PROP, *PVSS_MGMT_OBJECT_PROP
req.redist: 
ms.custom: 19H1
---

# VSS_MGMT_OBJECT_PROP structure


## -description


The <b>VSS_MGMT_OBJECT_PROP</b> structure 
    defines the properties of a volume, shadow copy storage volume, or a shadow copy storage 
    area.


## -struct-fields




### -field Type

Object type. For more information, see <a href="https://msdn.microsoft.com/ea28ff2c-6603-4193-9d5f-b41fffe28a90">VSS_MGMT_OBJECT_TYPE</a>.


### -field Obj

Management object properties: a union of 
       <a href="https://msdn.microsoft.com/f17765d5-ccb4-4ede-86e4-36ac80022da0">VSS_VOLUME_PROP</a>, 
       <a href="https://msdn.microsoft.com/c4a20583-7fee-4ae1-97ed-d80b2a7539e3">VSS_DIFF_VOLUME_PROP</a>, and  
       <a href="https://msdn.microsoft.com/9627d7b0-e9d0-425f-9051-cf4ab6b75a8c">VSS_DIFF_AREA_PROP</a> structures. (For more information, see 
       <a href="https://msdn.microsoft.com/en-us/library/Aa384957(v=VS.85).aspx">VSS_MGMT_OBJECT_UNION</a>.)

It contains information for an object of the type specified by the <b>Type</b> member. 
       Management objects can be volumes, shadow copy storage volumes, or shadow copy storage areas.


## -see-also




<a href="https://msdn.microsoft.com/0ddcf25d-dc3e-4522-a98e-98d867230d42">IVssEnumMgmtObject::Next</a>



<a href="https://msdn.microsoft.com/9627d7b0-e9d0-425f-9051-cf4ab6b75a8c">VSS_DIFF_AREA_PROP</a>



<a href="https://msdn.microsoft.com/c4a20583-7fee-4ae1-97ed-d80b2a7539e3">VSS_DIFF_VOLUME_PROP</a>



<a href="https://msdn.microsoft.com/ea28ff2c-6603-4193-9d5f-b41fffe28a90">VSS_MGMT_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa384957(v=VS.85).aspx">VSS_MGMT_OBJECT_UNION</a>



<a href="https://msdn.microsoft.com/f17765d5-ccb4-4ede-86e4-36ac80022da0">VSS_VOLUME_PROP</a>



<a href="https://msdn.microsoft.com/20cf12e4-4611-4e39-9f6f-e29f15e58b36">Volume Shadow Copy API Structures</a>
 

 

