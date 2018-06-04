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

# _VSS_OBJECT_TYPE enumeration


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



<a href="https://msdn.microsoft.com/e8d70f20-00a9-4cae-a92c-e3f3673a8db3">VSS_OBJECT_UNION</a>
 

 

