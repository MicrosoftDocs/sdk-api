---
UID: NF:winddi.EngFreePrivateUserMem
title: EngFreePrivateUserMem macro
author: windows-sdk-content
description: The EngFreePrivateUserMem function deallocates a block of private user memory.
old-location: display\engfreeprivateusermem.htm
tech.root: display
ms.assetid: 098bba48-849e-4a35-801c-9573bc5c33f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EngFreePrivateUserMem, EngFreePrivateUserMem function [Display Devices], display.engfreeprivateusermem, gdifncs_debf1b76-d783-4b91-832e-c95c2c41af76.xml, winddi/EngFreePrivateUserMem
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
 - EngFreePrivateUserMem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngFreePrivateUserMem macro


## -description


The <b>EngFreePrivateUserMem</b> function deallocates a block of private user memory.


## -parameters




### -param psl [in]

Pointer to the <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure representing the DirectDraw surface with which the memory is associated.


### -param p [in]

Pointer to the block of user memory being deallocated.


## -remarks



This routine deallocates a block of memory allocated by <a href="https://msdn.microsoft.com/416faebe-021b-4c00-9aba-d103a26348f6">EngAllocPrivateUserMem</a>. 




## -see-also




<a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a>



<a href="https://msdn.microsoft.com/416faebe-021b-4c00-9aba-d103a26348f6">EngAllocPrivateUserMem</a>



<a href="https://msdn.microsoft.com/5864d8dc-e239-4ba8-bd22-4a4a8952c39e">EngAllocUserMem</a>



<a href="https://msdn.microsoft.com/3d409288-697e-4fa7-8ca9-ae80335f48a2">EngFreeUserMem</a>
 

 

