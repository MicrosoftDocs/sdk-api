---
UID: NF:winddi.EngMapModule
title: EngMapModule function
author: windows-sdk-content
description: The EngMapModule function returns the address and size of a file that was loaded by EngLoadModule, EngLoadModuleForWrite, EngLoadImage, or EngMapFile.
old-location: display\engmapmodule.htm
old-project: display
ms.assetid: f8bd9b2c-11a3-454f-a4ce-cbda28115564
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: EngMapModule, EngMapModule function [Display Devices], display.engmapmodule, gdifncs_c3731e1a-e853-403b-958b-370494e79ae7.xml, winddi/EngMapModule
ms.prod: windows
ms.technology: windows-sdk
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
 - EngMapModule
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngMapModule function


## -description


The <b>EngMapModule</b> function returns the address and size of a file that was loaded by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff564963">EngLoadImage</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>.


## -parameters




### -param h [in]

Handle to the file to be memory-mapped.


### -param pSize [in]

Pointer to a memory location that receives the size, in bytes, of the memory-mapped file.


## -returns



<b>EngMapModule</b> returns a pointer to the view of the file identified by <i>h</i>.




## -remarks



A driver can open and read a file using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a> and <b>EngMapModule</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564902">EngFreeModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564963">EngLoadImage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>
 

 

