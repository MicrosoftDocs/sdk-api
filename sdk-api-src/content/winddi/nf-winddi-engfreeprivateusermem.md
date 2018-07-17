---
UID: NF:winddi.EngFreePrivateUserMem
title: EngFreePrivateUserMem macro
author: windows-sdk-content
description: The EngFreePrivateUserMem function deallocates a block of private user memory.
old-location: display\engfreeprivateusermem.htm
old-project: display
ms.assetid: 098bba48-849e-4a35-801c-9573bc5c33f5
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: EngFreePrivateUserMem, EngFreePrivateUserMem function [Display Devices], display.engfreeprivateusermem, gdifncs_debf1b76-d783-4b91-832e-c95c2c41af76.xml, winddi/EngFreePrivateUserMem
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
 - EngFreePrivateUserMem
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngFreePrivateUserMem macro


## -description


The <b>EngFreePrivateUserMem</b> function deallocates a block of private user memory.


## -parameters




### -param psl [in]

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure representing the DirectDraw surface with which the memory is associated.


### -param p

TBD






#### - pv [in]

Pointer to the block of user memory being deallocated.


## -remarks



This routine deallocates a block of memory allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564177">EngAllocPrivateUserMem</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564177">EngAllocPrivateUserMem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564178">EngAllocUserMem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564912">EngFreeUserMem</a>
 

 

