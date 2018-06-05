---
UID: NS:processsnapshot.PSS_VA_SPACE_INFORMATION
title: PSS_VA_SPACE_INFORMATION
author: windows-sdk-content
description: Holds virtual address (VA) space information returned by PssQuerySnapshot.
old-location: proc_snap\pss_va_space_information.htm
old-project: proc_snap
ms.assetid: F38FF7EB-DDC5-4692-8F57-8D633193D891
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: PSS_VA_SPACE_INFORMATION, PSS_VA_SPACE_INFORMATION structure, proc_snap.pss_va_space_information, processsnapshot/PSS_VA_SPACE_INFORMATION
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
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	processsnapshot.h
api_name:
-	PSS_VA_SPACE_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSS_VA_SPACE_INFORMATION structure


## -description


Holds virtual address (VA) space information returned by <a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a>.


## -struct-fields




### -field RegionCount

The count of VA regions captured.


## -remarks




<a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a> returns a <b>PSS_VA_SPACE_INFORMATION</b> structure when the <a href="https://msdn.microsoft.com/1C3E5BF4-5AC9-4012-B29D-49C35C0AF90B">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_VA_SPACE_INFORMATION</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

