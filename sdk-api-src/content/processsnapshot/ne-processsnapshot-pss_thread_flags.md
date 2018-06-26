---
UID: NE:processsnapshot.PSS_THREAD_FLAGS
title: PSS_THREAD_FLAGS
author: windows-sdk-content
description: Flags that describe a thread.
old-location: proc_snap\pss_thread_flags.htm
old-project: proc_snap
ms.assetid: 8E90F0EA-D50A-431D-9507-B882EB673629
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: PSS_THREAD_FLAGS, PSS_THREAD_FLAGS enumeration, PSS_THREAD_FLAGS_NONE, PSS_THREAD_FLAGS_TERMINATED, proc_snap.pss_thread_flags, processsnapshot/PSS_THREAD_FLAGS, processsnapshot/PSS_THREAD_FLAGS_NONE, processsnapshot/PSS_THREAD_FLAGS_TERMINATED
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PSS_THREAD_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_THREAD_FLAGS
product: Windows
targetos: Windows
req.lib: Prntvpt.lib
req.dll: Prntvpt.dll
req.irql: 
req.product: ADAM
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



There is a <b>PSS_THREAD_FLAGS</b> member in the <a href="https://msdn.microsoft.com/99C89DBB-8C12-482E-B33D-AE59C37662CF">PSS_THREAD_ENTRY</a> structure that <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a> returns.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

