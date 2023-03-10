---
UID: NS:processsnapshot.PSS_VA_SPACE_INFORMATION
title: PSS_VA_SPACE_INFORMATION (processsnapshot.h)
description: Holds virtual address (VA) space information returned by PssQuerySnapshot.
helpviewer_keywords: ["PSS_VA_SPACE_INFORMATION","PSS_VA_SPACE_INFORMATION structure","proc_snap.pss_va_space_information","processsnapshot/PSS_VA_SPACE_INFORMATION"]
old-location: proc_snap\pss_va_space_information.htm
tech.root: proc_snap
ms.assetid: F38FF7EB-DDC5-4692-8F57-8D633193D891
ms.date: 12/05/2018
ms.keywords: PSS_VA_SPACE_INFORMATION, PSS_VA_SPACE_INFORMATION structure, proc_snap.pss_va_space_information, processsnapshot/PSS_VA_SPACE_INFORMATION
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
req.typenames: PSS_VA_SPACE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_VA_SPACE_INFORMATION
 - processsnapshot/PSS_VA_SPACE_INFORMATION
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
 - PSS_VA_SPACE_INFORMATION
---

# PSS_VA_SPACE_INFORMATION structure


## -description

Holds virtual address (VA) space information returned by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a>.

## -struct-fields

### -field RegionCount

The count of VA regions captured.

## -remarks

<a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a> returns a <b>PSS_VA_SPACE_INFORMATION</b> structure when the <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_query_information_class">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_VA_SPACE_INFORMATION</b>.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>

