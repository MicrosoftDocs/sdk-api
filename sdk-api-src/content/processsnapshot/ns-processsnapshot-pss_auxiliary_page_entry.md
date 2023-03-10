---
UID: NS:processsnapshot.PSS_AUXILIARY_PAGE_ENTRY
title: PSS_AUXILIARY_PAGE_ENTRY (processsnapshot.h)
description: Holds auxiliary page entry information returned by PssWalkSnapshot.
helpviewer_keywords: ["PSS_AUXILIARY_PAGE_ENTRY","PSS_AUXILIARY_PAGE_ENTRY structure","proc_snap.pss_auxiliary_page_entry","processsnapshot/PSS_AUXILIARY_PAGE_ENTRY"]
old-location: proc_snap\pss_auxiliary_page_entry.htm
tech.root: proc_snap
ms.assetid: A3D948E6-6FFE-4732-A8C7-A292FDA07D7C
ms.date: 12/05/2018
ms.keywords: PSS_AUXILIARY_PAGE_ENTRY, PSS_AUXILIARY_PAGE_ENTRY structure, proc_snap.pss_auxiliary_page_entry, processsnapshot/PSS_AUXILIARY_PAGE_ENTRY
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
req.typenames: PSS_AUXILIARY_PAGE_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_AUXILIARY_PAGE_ENTRY
 - processsnapshot/PSS_AUXILIARY_PAGE_ENTRY
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
 - PSS_AUXILIARY_PAGE_ENTRY
---

# PSS_AUXILIARY_PAGE_ENTRY structure


## -description

Holds auxiliary page entry information returned by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a>.

## -struct-fields

### -field Address

The address of the captured auxiliary page, in the context of the captured process.

### -field BasicInformation

Basic information about the captured page. See <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a> for more information.

### -field CaptureTime

The capture time of the page. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field PageContents

A pointer to the contents of the captured page, in the context of the current process. This member may be <b>NULL</b> if page contents were not captured. The pointer is valid for the lifetime of the walk marker passed to <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a>.

### -field PageSize

The size of the page contents that <b>PageContents</b> points to, in bytes.

## -remarks

<a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a> returns a <b>PSS_AUXILIARY_PAGE_ENTRY</b> structure when the  <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_walk_information_class">PSS_WALK_INFORMATION_CLASS</a> member that the caller provides it is <b>PSS_WALK_AUXILIARY_PAGES</b>.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>

