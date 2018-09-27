---
UID: NS:processsnapshot.PSS_AUXILIARY_PAGES_INFORMATION
title: PSS_AUXILIARY_PAGES_INFORMATION
author: windows-sdk-content
description: Holds auxiliary pages information returned by PssQuerySnapshot.
old-location: proc_snap\pss_auxiliary_pages_information.htm
tech.root: proc_snap
ms.assetid: 122DD3DF-002A-4250-9E37-BA239638A684
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PSS_AUXILIARY_PAGES_INFORMATION, PSS_AUXILIARY_PAGES_INFORMATION structure, proc_snap.pss_auxiliary_pages_information, processsnapshot/PSS_AUXILIARY_PAGES_INFORMATION
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
 - PSS_AUXILIARY_PAGES_INFORMATION
product: Windows
targetos: Windows
req.typenames: PSS_AUXILIARY_PAGES_INFORMATION
req.redist: 
---

# PSS_AUXILIARY_PAGES_INFORMATION structure


## -description


Holds auxiliary pages information returned by <a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a>.


## -struct-fields




### -field AuxPagesCaptured

The count of auxiliary pages captured.


## -remarks




<a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a> returns a <b>PSS_AUXILIARY_PAGES_INFORMATION</b> structure when the <a href="https://msdn.microsoft.com/1C3E5BF4-5AC9-4012-B29D-49C35C0AF90B">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_AUXILIARY_PAGES_INFORMATION</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

