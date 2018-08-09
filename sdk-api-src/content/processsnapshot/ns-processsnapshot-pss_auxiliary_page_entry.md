---
UID: NS:processsnapshot.PSS_AUXILIARY_PAGE_ENTRY
title: PSS_AUXILIARY_PAGE_ENTRY
author: windows-sdk-content
description: Holds auxiliary page entry information returned by PssWalkSnapshot.
old-location: proc_snap\pss_auxiliary_page_entry.htm
old-project: proc_snap
ms.assetid: A3D948E6-6FFE-4732-A8C7-A292FDA07D7C
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: PSS_AUXILIARY_PAGE_ENTRY, PSS_AUXILIARY_PAGE_ENTRY structure, proc_snap.pss_auxiliary_page_entry, processsnapshot/PSS_AUXILIARY_PAGE_ENTRY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: PSS_AUXILIARY_PAGE_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_AUXILIARY_PAGE_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PSS_AUXILIARY_PAGE_ENTRY structure


## -description


Holds auxiliary page entry information returned by <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a>.


## -struct-fields




### -field Address

The address of the captured auxiliary page, in the context of the captured process.


### -field BasicInformation

Basic information about the captured page. See <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a> for more information.


### -field CaptureTime

The capture time of the page. For more information, see <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>.


### -field PageContents

A pointer to the contents of the captured page, in the context of the current process. This member may be <b>NULL</b> if page contents were not captured. The pointer is valid for the lifetime of the walk marker passed to <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a>.


### -field PageSize

The size of the page contents that <b>PageContents</b> points to, in bytes.


## -remarks




<a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a> returns a <b>PSS_AUXILIARY_PAGE_ENTRY</b> structure when the  <a href="https://msdn.microsoft.com/93A79F7F-2164-4F7A-ADE7-C1655EEFC9BF">PSS_WALK_INFORMATION_CLASS</a> member that the caller provides it is <b>PSS_WALK_AUXILIARY_PAGES</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

