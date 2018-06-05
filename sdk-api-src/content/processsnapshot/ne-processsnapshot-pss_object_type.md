---
UID: NE:processsnapshot.PSS_OBJECT_TYPE
title: PSS_OBJECT_TYPE
author: windows-sdk-content
description: Specifies the object type in a PSS_HANDLE_ENTRY structure.
old-location: proc_snap\pss_object_type.htm
old-project: proc_snap
ms.assetid: 3AF2AE47-6E1A-4B20-B6A3-36C1DDB80674
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: PSS_OBJECT_TYPE, PSS_OBJECT_TYPE enumeration, PSS_OBJECT_TYPE_EVENT, PSS_OBJECT_TYPE_MUTANT, PSS_OBJECT_TYPE_PROCESS, PSS_OBJECT_TYPE_SECTION, PSS_OBJECT_TYPE_THREAD, PSS_OBJECT_TYPE_UNKNOWN, proc_snap.pss_object_type, processsnapshot/PSS_OBJECT_TYPE, processsnapshot/PSS_OBJECT_TYPE_EVENT, processsnapshot/PSS_OBJECT_TYPE_MUTANT, processsnapshot/PSS_OBJECT_TYPE_PROCESS, processsnapshot/PSS_OBJECT_TYPE_SECTION, processsnapshot/PSS_OBJECT_TYPE_THREAD, processsnapshot/PSS_OBJECT_TYPE_UNKNOWN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: PSS_OBJECT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	processsnapshot.h
api_name:
-	PSS_OBJECT_TYPE
product: Windows
targetos: Windows
req.lib: Prntvpt.lib
req.dll: Prntvpt.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSS_OBJECT_TYPE enumeration


## -description


Specifies the object type in a <a href="https://msdn.microsoft.com/F56E8C35-949A-4DEE-973F-CF24F6596036">PSS_HANDLE_ENTRY</a> structure.


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




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

