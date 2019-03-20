---
UID: NE:vss._VSS_OBJECT_TYPE
title: VSS_OBJECT_TYPE (vss.h)
author: windows-sdk-content
description: Used by requesters to identify an object as a shadow copy set, shadow copy, or provider.
old-location: base\vss_object_type.htm
tech.root: VSS
ms.assetid: b7c91003-0ce7-463e-a816-c212da9dc31e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PVSS_OBJECT_TYPE, PVSS_OBJECT_TYPE, PVSS_OBJECT_TYPE enumeration pointer [VSS], VSS_OBJECT_NONE, VSS_OBJECT_PROVIDER, VSS_OBJECT_SNAPSHOT, VSS_OBJECT_SNAPSHOT_SET, VSS_OBJECT_TYPE, VSS_OBJECT_TYPE enumeration [VSS], VSS_OBJECT_TYPE_COUNT, VSS_OBJECT_UNKNOWN, _win32_vss_object_type, base.vss_object_type, vss/PVSS_OBJECT_TYPE, vss/VSS_OBJECT_NONE, vss/VSS_OBJECT_PROVIDER, vss/VSS_OBJECT_SNAPSHOT, vss/VSS_OBJECT_SNAPSHOT_SET, vss/VSS_OBJECT_TYPE, vss/VSS_OBJECT_TYPE_COUNT, vss/VSS_OBJECT_UNKNOWN"
ms.topic: enum
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
 - VSS_OBJECT_TYPE
product: Windows
targetos: Windows
req.typenames: VSS_OBJECT_TYPE, *PVSS_OBJECT_TYPE
req.redist: 
---

# VSS_OBJECT_TYPE enumeration


## -description


The <b>VSS_OBJECT_TYPE</b> enumeration is used by 
    requesters to identify an object as a shadow copy set, shadow copy, or provider.


## -enum-fields




### -field VSS_OBJECT_UNKNOWN

The object type is not known.
      

This indicates an application error.


### -field VSS_OBJECT_NONE

The interpretation of this value depends on whether it is used as an input to a VSS method or returned as 
      an output from a VSS method. 
      

When used as an input to a VSS method, it indicates that the method is not restricted to any particular 
       object type, but should act on all appropriate objects. In this sense, 
       <b>VSS_OBJECT_NONE</b> can be thought of as a wildcard input.

When returned as an output, the object type is not known and means that there has been an application 
       error.


### -field VSS_OBJECT_SNAPSHOT_SET

Shadow copy set.


### -field VSS_OBJECT_SNAPSHOT

Shadow copy.


### -field VSS_OBJECT_PROVIDER

Shadow copy provider.


### -field VSS_OBJECT_TYPE_COUNT

Reserved value.


## -remarks



<b>VSS_OBJECT_TYPE</b> is used when calling 
    <a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a> to specify the 
    types of objects about which to obtain information. An input of <b>VSS_OBJECT_NONE</b> will 
    return information about all objects.

In addition, <b>VSS_OBJECT_TYPE</b> is used as an input to 
    <a href="https://msdn.microsoft.com/2e06f69e-8210-4773-8080-5c58e6f59792">IVssBackupComponents::DeleteSnapshots</a>. 
    However, <b>DeleteSnapshots</b> accepts 
    only <b>VSS_OBJECT_TYPE</b> values of 
    <b>VSS_OBJECT_SNAPSHOT_SET</b> or <b>VSS_OBJECT_SNAPSHOT</b>.

The <b>Type</b> member of 
    <a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> is a member of the 
    <b>VSS_OBJECT_TYPE</b> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/2e06f69e-8210-4773-8080-5c58e6f59792">IVssBackupComponents::DeleteSnapshots</a>



<a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a>



<a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>



<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa384960(v=VS.85).aspx">VSS_OBJECT_UNION</a>
 

 

