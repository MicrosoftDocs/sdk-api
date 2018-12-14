---
UID: NS:processsnapshot.__unnamed_struct_6
title: PSS_HANDLE_TRACE_INFORMATION
author: windows-sdk-content
description: Holds handle trace information returned by PssQuerySnapshot.
old-location: proc_snap\pss_handle_trace_information.htm
tech.root: proc_snap
ms.assetid: 0877DF1F-044C-48F2-9BCC-938EBD6D46EE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSS_HANDLE_TRACE_INFORMATION, PSS_HANDLE_TRACE_INFORMATION structure, proc_snap.pss_handle_trace_information, processsnapshot/PSS_HANDLE_TRACE_INFORMATION
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PSS_HANDLE_TRACE_INFORMATION
product: Windows
targetos: Windows
req.typenames: PSS_HANDLE_TRACE_INFORMATION
req.redist: 
---

# PSS_HANDLE_TRACE_INFORMATION structure


## -description


Holds handle trace information returned by <a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a>.


## -struct-fields




### -field SectionHandle

A handle to a section containing the handle trace information.


### -field Size

The size of the handle trace section, in bytes.


## -remarks




<a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a> returns a <b>PSS_HANDLE_TRACE_INFORMATION</b> structure when the <a href="https://msdn.microsoft.com/en-us/library/Dn457851(v=VS.85).aspx">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_HANDLE_TRACE_INFORMATION</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

