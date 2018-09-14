---
UID: NF:winddi.EngFreeModule
title: EngFreeModule function
author: windows-sdk-content
description: The EngFreeModule function unmaps a file from system memory.
old-location: display\engfreemodule.htm
tech.root: display
ms.assetid: f5520aec-5747-4970-ba2f-06b39e4f43f2
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: EngFreeModule, EngFreeModule function [Display Devices], display.engfreemodule, gdifncs_23d84e6d-60e7-43a4-af20-3234c8581190.xml, winddi/EngFreeModule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - Ext-MS-Win-moderncore-Win32k-base-ntgdi-l1-1-0.dll
 - win32kfull.sys
 - win32kmin.sys
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngFreeModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngFreeModule function


## -description


The <b>EngFreeModule</b> function unmaps a file from system memory.


## -parameters




### -param h [in]

Handle to the memory-mapped file to be freed. This handle was obtained from <a href="https://msdn.microsoft.com/0327d3f0-f9ee-4715-aa0e-ad1d0544a1ff">EngLoadModule</a> or <a href="https://msdn.microsoft.com/e5509142-624e-4c57-93b0-2579c6fb7089">EngLoadModuleForWrite</a>.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/0327d3f0-f9ee-4715-aa0e-ad1d0544a1ff">EngLoadModule</a>



<a href="https://msdn.microsoft.com/e5509142-624e-4c57-93b0-2579c6fb7089">EngLoadModuleForWrite</a>



<a href="https://msdn.microsoft.com/f8bd9b2c-11a3-454f-a4ce-cbda28115564">EngMapModule</a>
 

 

