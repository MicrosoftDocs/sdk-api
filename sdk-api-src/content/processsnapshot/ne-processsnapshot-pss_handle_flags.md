---
UID: NE:processsnapshot.__unnamed_enum_0
title: PSS_HANDLE_FLAGS (processsnapshot.h)
description: Flags to specify what parts of a PSS_HANDLE_ENTRY structure are valid.
helpviewer_keywords: ["PSS_HANDLE_FLAGS","PSS_HANDLE_FLAGS enumeration","PSS_HANDLE_HAVE_BASIC_INFORMATION","PSS_HANDLE_HAVE_NAME","PSS_HANDLE_HAVE_TYPE","PSS_HANDLE_HAVE_TYPE_SPECIFIC_INFORMATION","PSS_HANDLE_NONE","proc_snap.pss_handle_flags","processsnapshot/PSS_HANDLE_FLAGS","processsnapshot/PSS_HANDLE_HAVE_BASIC_INFORMATION","processsnapshot/PSS_HANDLE_HAVE_NAME","processsnapshot/PSS_HANDLE_HAVE_TYPE","processsnapshot/PSS_HANDLE_HAVE_TYPE_SPECIFIC_INFORMATION","processsnapshot/PSS_HANDLE_NONE"]
old-location: proc_snap\pss_handle_flags.htm
tech.root: proc_snap
ms.assetid: A4A604A9-0210-413C-BCAC-F8458B371D42
ms.date: 12/05/2018
ms.keywords: PSS_HANDLE_FLAGS, PSS_HANDLE_FLAGS enumeration, PSS_HANDLE_HAVE_BASIC_INFORMATION, PSS_HANDLE_HAVE_NAME, PSS_HANDLE_HAVE_TYPE, PSS_HANDLE_HAVE_TYPE_SPECIFIC_INFORMATION, PSS_HANDLE_NONE, proc_snap.pss_handle_flags, processsnapshot/PSS_HANDLE_FLAGS, processsnapshot/PSS_HANDLE_HAVE_BASIC_INFORMATION, processsnapshot/PSS_HANDLE_HAVE_NAME, processsnapshot/PSS_HANDLE_HAVE_TYPE, processsnapshot/PSS_HANDLE_HAVE_TYPE_SPECIFIC_INFORMATION, processsnapshot/PSS_HANDLE_NONE
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
req.typenames: PSS_HANDLE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_HANDLE_FLAGS
 - processsnapshot/PSS_HANDLE_FLAGS
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
 - PSS_HANDLE_FLAGS
---

# PSS_HANDLE_FLAGS enumeration


## -description

Flags to specify what parts of a <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_handle_entry">PSS_HANDLE_ENTRY</a> structure are valid.

## -enum-fields

### -field PSS_HANDLE_NONE:0x00

No parts specified.

### -field PSS_HANDLE_HAVE_TYPE:0x01

The <b>ObjectType</b> member is valid.

### -field PSS_HANDLE_HAVE_NAME:0x02

The <b>ObjectName</b> member is valid.

### -field PSS_HANDLE_HAVE_BASIC_INFORMATION:0x04

The <b>Attributes</b>, <b>GrantedAccess</b>, <b>HandleCount</b>, <b>PointerCount</b>, <b>PagedPoolCharge</b>, and <b>NonPagedPoolCharge</b> members are valid.

### -field PSS_HANDLE_HAVE_TYPE_SPECIFIC_INFORMATION:0x08

The <b>TypeSpecificInformation</b> member is valid (either <b>Process</b>, <b>Thread</b>, <b>Mutant</b>, <b>Event</b> or <b>Section</b>).

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
