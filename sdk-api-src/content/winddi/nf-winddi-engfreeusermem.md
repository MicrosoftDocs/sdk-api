---
UID: NF:winddi.EngFreeUserMem
title: EngFreeUserMem macro
author: windows-sdk-content
description: The EngFreeUserMem function deallocates a block of user memory.
old-location: display\engfreeusermem.htm
old-project: display
ms.assetid: 3d409288-697e-4fa7-8ca9-ae80335f48a2
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: EngFreeUserMem, EngFreeUserMem function [Display Devices], display.engfreeusermem, gdifncs_954f4161-3780-41ac-9a53-fa60051cc637.xml, winddi/EngFreeUserMem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
 - EngFreeUserMem
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngFreeUserMem macro


## -description


The <b>EngFreeUserMem</b> function deallocates a block of user memory.


## -parameters




### -param p [in]

Pointer to the block of user memory being deallocated.


## -remarks



This routine releases memory allocated by <a href="https://msdn.microsoft.com/5864d8dc-e239-4ba8-bd22-4a4a8952c39e">EngAllocUserMem</a>. The memory block must not be accessed after it is freed.




## -see-also




<a href="https://msdn.microsoft.com/5864d8dc-e239-4ba8-bd22-4a4a8952c39e">EngAllocUserMem</a>
 

 

