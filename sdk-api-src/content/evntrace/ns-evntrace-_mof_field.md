---
UID: NS:evntrace._MOF_FIELD
title: "_MOF_FIELD"
author: windows-sdk-content
description: You may use the MOF_FIELD structures to append event data to the EVENT_TRACE_HEADER or EVENT_INSTANCE_HEADER structures.
old-location: etw\mof_field.htm
old-project: etw
ms.assetid: 64ff1191-2177-4d51-afcd-b58d510e9ae8
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: "*PMOF_FIELD, MOF_FIELD, MOF_FIELD structure [ETW], PMOF_FIELD, PMOF_FIELD structure pointer [ETW], _MOF_FIELD, _evt_mof_field, base.mof_field, etw.mof_field, evntrace/MOF_FIELD, evntrace/PMOF_FIELD"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MOF_FIELD, *PMOF_FIELD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntrace.h
api_name:
 - MOF_FIELD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _MOF_FIELD structure


## -description


You may use the <b>MOF_FIELD</b> structures to append event data to the 
<a href="https://msdn.microsoft.com/33c2de6b-afc2-4323-8d81-2970e66edf5e">EVENT_TRACE_HEADER</a> or 
<a href="https://msdn.microsoft.com/2a79d937-2a3b-4426-b31f-a1a3ce86a334">EVENT_INSTANCE_HEADER</a> structures.
		


## -struct-fields




### -field DataPtr

Pointer to a event data item.


### -field Length

Length of the item pointed to by <b>DataPtr</b>, in bytes.


### -field DataType

Reserved.


## -remarks



Be sure to initialize the memory for this structure to zero before setting any members.

If you use 
<b>MOF_FIELD</b> structures, you must set the <b>WNODE_FLAG_USE_MOF_PTR</b> flag in the <b>Flags</b> member of the 
<a href="https://msdn.microsoft.com/33c2de6b-afc2-4323-8d81-2970e66edf5e">EVENT_TRACE_HEADER</a> or 
<a href="https://msdn.microsoft.com/2a79d937-2a3b-4426-b31f-a1a3ce86a334">EVENT_INSTANCE_HEADER</a> structure.

The event tracing session automatically dereferences 
<b>MOF_FIELD</b> data pointers before passing the data to event trace consumers using 
<a href="https://msdn.microsoft.com/d8a6b63e-0cd4-4d19-b0b3-16bb0d33e4c0">EVENT_TRACE</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/2a79d937-2a3b-4426-b31f-a1a3ce86a334">EVENT_INSTANCE_HEADER</a>



<a href="https://msdn.microsoft.com/d8a6b63e-0cd4-4d19-b0b3-16bb0d33e4c0">EVENT_TRACE</a>



<a href="https://msdn.microsoft.com/33c2de6b-afc2-4323-8d81-2970e66edf5e">EVENT_TRACE_HEADER</a>
 

 

