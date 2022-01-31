---
UID: NE:processsnapshot.__unnamed_enum_5
title: PSS_DUPLICATE_FLAGS (processsnapshot.h)
description: Duplication flags for use by PssDuplicateSnapshot.
helpviewer_keywords: ["PSS_DUPLICATE_CLOSE_SOURCE","PSS_DUPLICATE_FLAGS","PSS_DUPLICATE_FLAGS enumeration","PSS_DUPLICATE_NONE","proc_snap.pss_duplicate_flags","processsnapshot/PSS_DUPLICATE_CLOSE_SOURCE","processsnapshot/PSS_DUPLICATE_FLAGS","processsnapshot/PSS_DUPLICATE_NONE"]
old-location: proc_snap\pss_duplicate_flags.htm
tech.root: proc_snap
ms.assetid: CAD06441-750F-42FC-A95A-7CAA79F31348
ms.date: 12/05/2018
ms.keywords: PSS_DUPLICATE_CLOSE_SOURCE, PSS_DUPLICATE_FLAGS, PSS_DUPLICATE_FLAGS enumeration, PSS_DUPLICATE_NONE, proc_snap.pss_duplicate_flags, processsnapshot/PSS_DUPLICATE_CLOSE_SOURCE, processsnapshot/PSS_DUPLICATE_FLAGS, processsnapshot/PSS_DUPLICATE_NONE
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
targetos: Windows
req.typenames: PSS_DUPLICATE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_DUPLICATE_FLAGS
 - processsnapshot/PSS_DUPLICATE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_DUPLICATE_FLAGS
---

# PSS_DUPLICATE_FLAGS enumeration


## -description

Duplication flags for use by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssduplicatesnapshot">PssDuplicateSnapshot</a>.

## -enum-fields

### -field PSS_DUPLICATE_NONE:0x00

No flag.

### -field PSS_DUPLICATE_CLOSE_SOURCE:0x01

Free the source handle. This will only succeed if you set the  <b>PSS_CREATE_USE_VM_ALLOCATIONS</b> flag when you called <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psscapturesnapshot">PssCaptureSnapshot</a> to create the snapshot and handle. The handle will be freed  even if duplication fails.
The close operation does not protect against concurrent access to the same descriptor.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
