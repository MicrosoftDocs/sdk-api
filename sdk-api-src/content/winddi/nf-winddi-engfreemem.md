---
UID: NF:winddi.EngFreeMem
title: EngFreeMem macro
author: windows-sdk-content
description: The EngFreeMem function deallocates a block of system memory.
old-location: display\engfreemem.htm
tech.root: display
ms.assetid: 04428d7e-4150-4e68-a660-0a9e246c82ae
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: EngFreeMem, EngFreeMem function [Display Devices], display.engfreemem, gdifncs_4479237b-46a6-40a1-a9ad-dd1cd0a4c4bb.xml, winddi/EngFreeMem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngFreeMem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngFreeMem macro


## -description


The <b>EngFreeMem</b> function deallocates a block of system memory.


## -parameters




### -param p [in]

Pointer to the block of memory being deallocated.


## -remarks



This routine releases memory allocated by <a href="https://msdn.microsoft.com/61bef5a1-bf68-4d37-ae5d-13ff045a2344">EngAllocMem</a>. The memory block must not be accessed after it is freed.




## -see-also




<a href="https://msdn.microsoft.com/61bef5a1-bf68-4d37-ae5d-13ff045a2344">EngAllocMem</a>
 

 

