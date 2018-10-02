---
UID: NS:processsnapshot.PSS_THREAD_INFORMATION
title: PSS_THREAD_INFORMATION
author: windows-sdk-content
description: Holds thread information returned by PssQuerySnapshot.
old-location: proc_snap\pss_thread_information.htm
tech.root: proc_snap
ms.assetid: 68BC42FD-9A30-462F-AFB1-DF9587C50F45
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PSS_THREAD_INFORMATION, PSS_THREAD_INFORMATION structure, proc_snap.pss_thread_information, processsnapshot/PSS_THREAD_INFORMATION
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
 - PSS_THREAD_INFORMATION
product: Windows
targetos: Windows
req.typenames: PSS_THREAD_INFORMATION
req.redist: 
---

# PSS_THREAD_INFORMATION structure


## -description


Holds thread information returned by <a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a>.


## -struct-fields




### -field ThreadsCaptured

The count of threads in the snapshot.


### -field ContextLength

The length of the <b>CONTEXT</b> record captured, in bytes.


## -remarks




<a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a> returns a <b>PSS_THREAD_INFORMATION</b> structure when the <a href="https://msdn.microsoft.com/1C3E5BF4-5AC9-4012-B29D-49C35C0AF90B">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_THREAD_INFORMATION</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

