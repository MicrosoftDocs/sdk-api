---
UID: NF:winddi.EngFreeMem
title: EngFreeMem macro
author: windows-sdk-content
description: The EngFreeMem function deallocates a block of system memory.
old-location: display\engfreemem.htm
old-project: display
ms.assetid: 04428d7e-4150-4e68-a660-0a9e246c82ae
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngFreeMem, EngFreeMem function [Display Devices], display.engfreemem, gdifncs_4479237b-46a6-40a1-a9ad-dd1cd0a4c4bb.xml, winddi/EngFreeMem
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngFreeMem macro


## -description


The <b>EngFreeMem</b> function deallocates a block of system memory.


## -parameters




### -param p

TBD






#### - Mem [in]

Pointer to the block of memory being deallocated.


## -remarks



This routine releases memory allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564176">EngAllocMem</a>. The memory block must not be accessed after it is freed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564176">EngAllocMem</a>
 

 

