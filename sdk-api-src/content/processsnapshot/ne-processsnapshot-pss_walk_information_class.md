---
UID: NE:processsnapshot.__unnamed_enum_4
title: PSS_WALK_INFORMATION_CLASS (processsnapshot.h)
description: Specifies what information the PssWalkSnapshot function returns.
helpviewer_keywords: ["PSS_WALK_AUXILIARY_PAGES","PSS_WALK_HANDLES","PSS_WALK_INFORMATION_CLASS","PSS_WALK_INFORMATION_CLASS enumeration","PSS_WALK_THREADS","PSS_WALK_VA_SPACE","proc_snap.pss_walk_information_class","processsnapshot/PSS_WALK_AUXILIARY_PAGES","processsnapshot/PSS_WALK_HANDLES","processsnapshot/PSS_WALK_INFORMATION_CLASS","processsnapshot/PSS_WALK_THREADS","processsnapshot/PSS_WALK_VA_SPACE"]
old-location: proc_snap\pss_walk_information_class.htm
tech.root: proc_snap
ms.assetid: 93A79F7F-2164-4F7A-ADE7-C1655EEFC9BF
ms.date: 12/05/2018
ms.keywords: PSS_WALK_AUXILIARY_PAGES, PSS_WALK_HANDLES, PSS_WALK_INFORMATION_CLASS, PSS_WALK_INFORMATION_CLASS enumeration, PSS_WALK_THREADS, PSS_WALK_VA_SPACE, proc_snap.pss_walk_information_class, processsnapshot/PSS_WALK_AUXILIARY_PAGES, processsnapshot/PSS_WALK_HANDLES, processsnapshot/PSS_WALK_INFORMATION_CLASS, processsnapshot/PSS_WALK_THREADS, processsnapshot/PSS_WALK_VA_SPACE
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
req.typenames: PSS_WALK_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_WALK_INFORMATION_CLASS
 - processsnapshot/PSS_WALK_INFORMATION_CLASS
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
 - PSS_WALK_INFORMATION_CLASS
---

# PSS_WALK_INFORMATION_CLASS enumeration


## -description

Specifies what information the <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a> function returns.

## -enum-fields

### -field PSS_WALK_AUXILIARY_PAGES:0

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_auxiliary_page_entry">PSS_AUXILIARY_PAGE_ENTRY</a> structure, which contains the address, page attributes and contents of an auxiliary copied page.

### -field PSS_WALK_VA_SPACE:1

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_va_space_entry">PSS_VA_SPACE_ENTRY</a> structure, which contains the <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a> structure for every distinct VA region.

### -field PSS_WALK_HANDLES:2

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_handle_entry">PSS_HANDLE_ENTRY</a> structure, with information specifying the handle value, its type name, object name (if captured), basic information (if captured), and type-specific information (if captured).

### -field PSS_WALK_THREADS:3

Returns a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_thread_entry">PSS_THREAD_ENTRY</a> structure, with basic information about the thread, as well as its termination state, suspend count and Win32 start address.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
