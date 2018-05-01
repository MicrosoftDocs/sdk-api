---
UID: NS:processsnapshot.PSS_VA_CLONE_INFORMATION
title: PSS_VA_CLONE_INFORMATION
author: windows-driver-content
description: Holds virtual address (VA) clone information returned by PssQuerySnapshot.
old-location: proc_snap\pss_va_clone_information.htm
old-project: proc_snap
ms.assetid: F93D61B0-EDB2-4560-A69F-CF839EC98B53
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PSS_VA_CLONE_INFORMATION, PSS_VA_CLONE_INFORMATION structure, proc_snap.pss_va_clone_information, processsnapshot/PSS_VA_CLONE_INFORMATION
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
req.typenames: PSS_VA_CLONE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	processsnapshot.h
api_name:
-	PSS_VA_CLONE_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PSS_VA_CLONE_INFORMATION structure


## -description


Holds virtual address (VA) clone information returned by <a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a>.


## -struct-fields




### -field VaCloneHandle

A handle to the VA clone process.


## -remarks




<a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a> returns a <b>PSS_VA_CLONE_INFORMATION</b> structure when the <a href="https://msdn.microsoft.com/1C3E5BF4-5AC9-4012-B29D-49C35C0AF90B">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_VA_CLONE_INFORMATION</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

