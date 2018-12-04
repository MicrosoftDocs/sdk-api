---
UID: NE:processsnapshot.__unnamed_enum_5
title: PSS_DUPLICATE_FLAGS
author: windows-sdk-content
description: Duplication flags for use by PssDuplicateSnapshot.
old-location: proc_snap\pss_duplicate_flags.htm
tech.root: proc_snap
ms.assetid: CAD06441-750F-42FC-A95A-7CAA79F31348
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PSS_DUPLICATE_CLOSE_SOURCE, PSS_DUPLICATE_FLAGS, PSS_DUPLICATE_FLAGS enumeration, PSS_DUPLICATE_NONE, proc_snap.pss_duplicate_flags, processsnapshot/PSS_DUPLICATE_CLOSE_SOURCE, processsnapshot/PSS_DUPLICATE_FLAGS, processsnapshot/PSS_DUPLICATE_NONE
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PSS_DUPLICATE_FLAGS
product: Windows
targetos: Windows
req.typenames: PSS_DUPLICATE_FLAGS
req.redist: 
---

# PSS_DUPLICATE_FLAGS enumeration


## -description


Duplication flags for use by <a href="https://msdn.microsoft.com/5D2751F3-E7E1-4917-8060-E2BC8A7A3DEA">PssDuplicateSnapshot</a>.


## -enum-fields




### -field PSS_DUPLICATE_NONE

No flag.


### -field PSS_DUPLICATE_CLOSE_SOURCE

Free the source handle. This will only succeed if you set the  <b>PSS_CREATE_USE_VM_ALLOCATIONS</b> flag when you called <a href="https://msdn.microsoft.com/44F2CB48-A9F6-4131-B21C-9F27A27CECD5">PssCaptureSnapshot</a> to create the snapshot and handle. The handle will be freed  even if duplication fails.
The close operation does not protect against concurrent access to the same descriptor.


## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

