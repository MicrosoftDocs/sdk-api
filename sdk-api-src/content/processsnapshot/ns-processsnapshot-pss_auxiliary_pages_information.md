---
UID: NS:processsnapshot.__unnamed_struct_2
title: PSS_AUXILIARY_PAGES_INFORMATION (processsnapshot.h)
description: Holds auxiliary pages information returned by PssQuerySnapshot.
old-location: proc_snap\pss_auxiliary_pages_information.htm
tech.root: proc_snap
ms.assetid: 122DD3DF-002A-4250-9E37-BA239638A684
ms.date: 12/05/2018
ms.keywords: PSS_AUXILIARY_PAGES_INFORMATION, PSS_AUXILIARY_PAGES_INFORMATION structure, proc_snap.pss_auxiliary_pages_information, processsnapshot/PSS_AUXILIARY_PAGES_INFORMATION
ms.topic: struct
f1_keywords:
- processsnapshot/PSS_AUXILIARY_PAGES_INFORMATION
dev_langs:
- c++
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
- PSS_AUXILIARY_PAGES_INFORMATION
targetos: Windows
req.typenames: PSS_AUXILIARY_PAGES_INFORMATION
req.redist: 
ms.custom: 19H1
---

# PSS_AUXILIARY_PAGES_INFORMATION structure


## -description


Holds auxiliary pages information returned by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a>.


## -struct-fields




### -field AuxPagesCaptured

The count of auxiliary pages captured.


## -remarks




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a> returns a <b>PSS_AUXILIARY_PAGES_INFORMATION</b> structure when the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_query_information_class">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_AUXILIARY_PAGES_INFORMATION</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
 

 

