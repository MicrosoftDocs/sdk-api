---
UID: NE:processsnapshot.__unnamed_enum_1
title: PSS_OBJECT_TYPE (processsnapshot.h)
author: windows-sdk-content
description: Specifies the object type in a PSS_HANDLE_ENTRY structure.
old-location: proc_snap\pss_object_type.htm
tech.root: proc_snap
ms.assetid: 3AF2AE47-6E1A-4B20-B6A3-36C1DDB80674
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PSS_OBJECT_TYPE, PSS_OBJECT_TYPE enumeration, PSS_OBJECT_TYPE_EVENT, PSS_OBJECT_TYPE_MUTANT, PSS_OBJECT_TYPE_PROCESS, PSS_OBJECT_TYPE_SECTION, PSS_OBJECT_TYPE_THREAD, PSS_OBJECT_TYPE_UNKNOWN, proc_snap.pss_object_type, processsnapshot/PSS_OBJECT_TYPE, processsnapshot/PSS_OBJECT_TYPE_EVENT, processsnapshot/PSS_OBJECT_TYPE_MUTANT, processsnapshot/PSS_OBJECT_TYPE_PROCESS, processsnapshot/PSS_OBJECT_TYPE_SECTION, processsnapshot/PSS_OBJECT_TYPE_THREAD, processsnapshot/PSS_OBJECT_TYPE_UNKNOWN
ms.topic: enum
f1_keywords: 
 - "processsnapshot/PSS_OBJECT_TYPE"
req.header: processsnapshot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - processsnapshot.h
api_name:
 - PSS_OBJECT_TYPE
product: Windows
targetos: Windows
req.typenames: PSS_OBJECT_TYPE
req.redist: 
ms.custom: 19H1
---

# PSS_OBJECT_TYPE enumeration


## -description


Specifies the object type in a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_handle_entry">PSS_HANDLE_ENTRY</a> structure.


## -enum-fields




### -field PSS_OBJECT_TYPE_UNKNOWN

The object type is either unknown or unsupported.


### -field PSS_OBJECT_TYPE_PROCESS

The object is a process.


### -field PSS_OBJECT_TYPE_THREAD

The object is a thread. 


### -field PSS_OBJECT_TYPE_MUTANT

The object is a mutant/mutex.


### -field PSS_OBJECT_TYPE_EVENT

The object is an event.


### -field PSS_OBJECT_TYPE_SECTION

The object is a file-mapping object.


### -field PSS_OBJECT_TYPE_SEMAPHORE




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
 

 

