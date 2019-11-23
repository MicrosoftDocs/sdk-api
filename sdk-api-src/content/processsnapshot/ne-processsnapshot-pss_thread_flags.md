---
UID: NE:processsnapshot.__unnamed_enum_7
title: PSS_THREAD_FLAGS (processsnapshot.h)

description: Flags that describe a thread.
old-location: proc_snap\pss_thread_flags.htm
tech.root: proc_snap
ms.assetid: 8E90F0EA-D50A-431D-9507-B882EB673629

ms.date: 12/05/2018
ms.keywords: PSS_THREAD_FLAGS, PSS_THREAD_FLAGS enumeration, PSS_THREAD_FLAGS_NONE, PSS_THREAD_FLAGS_TERMINATED, proc_snap.pss_thread_flags, processsnapshot/PSS_THREAD_FLAGS, processsnapshot/PSS_THREAD_FLAGS_NONE, processsnapshot/PSS_THREAD_FLAGS_TERMINATED
ms.topic: enum
f1_keywords: 
 - "processsnapshot/PSS_THREAD_FLAGS"
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
 - PSS_THREAD_FLAGS
targetos: Windows
req.typenames: PSS_THREAD_FLAGS
req.redist: 
ms.custom: 19H1
---

# PSS_THREAD_FLAGS enumeration


## -description


Flags that describe a thread.


## -enum-fields




### -field PSS_THREAD_FLAGS_NONE

No flag.


### -field PSS_THREAD_FLAGS_TERMINATED

The thread terminated.


## -remarks



There is a <b>PSS_THREAD_FLAGS</b> member in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_thread_entry">PSS_THREAD_ENTRY</a> structure that <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a> returns.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
 

 

