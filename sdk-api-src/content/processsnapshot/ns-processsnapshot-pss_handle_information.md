---
UID: NS:processsnapshot.PSS_HANDLE_INFORMATION
title: PSS_HANDLE_INFORMATION (processsnapshot.h)
description: Holds handle information returned by PssQuerySnapshot.
helpviewer_keywords: ["PSS_HANDLE_INFORMATION","PSS_HANDLE_INFORMATION structure","proc_snap.pss_handle_information","processsnapshot/PSS_HANDLE_INFORMATION"]
old-location: proc_snap\pss_handle_information.htm
tech.root: proc_snap
ms.assetid: 77192849-D919-4947-9BFF-343C166C5A51
ms.date: 12/05/2018
ms.keywords: PSS_HANDLE_INFORMATION, PSS_HANDLE_INFORMATION structure, proc_snap.pss_handle_information, processsnapshot/PSS_HANDLE_INFORMATION
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
req.typenames: PSS_HANDLE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_HANDLE_INFORMATION
 - processsnapshot/PSS_HANDLE_INFORMATION
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
 - PSS_HANDLE_INFORMATION
---

# PSS_HANDLE_INFORMATION structure


## -description

Holds handle information returned by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a>.

## -struct-fields

### -field HandlesCaptured

The count of handles captured.

## -remarks

<a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a> returns a <b>PSS_HANDLE_INFORMATION</b> structure when the <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_query_information_class">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_HANDLE_INFORMATION</b>.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>

