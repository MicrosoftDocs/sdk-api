---
UID: NS:winperf._PERF_INSTANCE_DEFINITION
title: "_PERF_INSTANCE_DEFINITION"
author: windows-sdk-content
description: Describes an instance of a performance object.
old-location: perf\perf_instance_definition_str.htm
old-project: perfctrs
ms.assetid: 5ea617d3-857d-4e0a-ad10-4d63044fc927
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*PPERF_INSTANCE_DEFINITION, PERF_INSTANCE_DEFINITION, PERF_INSTANCE_DEFINITION structure [Perf], _PERF_INSTANCE_DEFINITION, _win32_perf_instance_definition_str, base.perf_instance_definition_str, perf.perf_instance_definition_str, winperf/PERF_INSTANCE_DEFINITION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winperf.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: PERF_INSTANCE_DEFINITION, *PPERF_INSTANCE_DEFINITION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winperf.h
api_name:
 - PERF_INSTANCE_DEFINITION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PERF_INSTANCE_DEFINITION structure


## -description


Describes an instance of a performance object.


## -struct-fields




### -field ByteLength

Size of this structure, including the instance name that follows, in bytes. This value must be an 8-byte multiple.


### -field ParentObjectTitleIndex

Index of the name of the parent object in the title database. For example, if the object is a thread, the parent object is a process, or if the object is a logical drive, the parent is a physical drive.


### -field ParentObjectInstance

Position of the instance within the parent object that is associated with this instance. The position is zero-based.


### -field UniqueID

A unique identifier that you can use to identify the instance instead of
                                        using the name to identify
                                        the instance. If you do not use unique identifiers to distinguish the counter instances, set this member to PERF_NO_UNIQUE_ID.


### -field NameOffset

Offset from the beginning of this structure to the Unicode name of this instance. 


### -field NameLength

Length of the instance name, including the null-terminator, in bytes. This member is zero if the instance does not have a name. 

Do not include in the length any padding that you added to the instance name to ensure that <b>ByteLength</b> is aligned to an 8-byte boundary. 


## -remarks



The object contains instances if the <b>NumInstances</b>  member of <a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a> is greater than zero. Use the <b>DefinitionLength</b> member of <b>PERF_OBJECT_TYPE</b> to find the first instance of the object. For details, see <a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>.

Consumers should use the parent instance name, if specified, to create a full instance name that is used for display. The convention is to form the name as parent/child.

Providers should use unique instance names. If you do not, it makes it difficult for consumers to calculate and display performance values because they cannot tell if the current instance refers to the same instance that was queried previously (instances can come and go). 

Providers must allocate enough space for the instance name to ensure that <b>ByteLength</b> is aligned to an 8-byte boundary. 




## -see-also




<a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a>
 

 

