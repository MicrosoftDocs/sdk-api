---
UID: NF:winddi.EngFreeModule
title: EngFreeModule function
author: windows-driver-content
description: The EngFreeModule function unmaps a file from system memory.
old-location: display\engfreemodule.htm
old-project: display
ms.assetid: f5520aec-5747-4970-ba2f-06b39e4f43f2
ms.author: windowsdriverdev
ms.date: 5/8/2018
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
-	Ext-MS-Win-moderncore-Win32k-base-ntgdi-l1-1-0.dll
-	win32kfull.sys
-	win32kmin.sys
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32.dll
-	GDI32Full.dll
api_name:
-	EngFreeModule
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngFreeModule function


## -description


The <b>EngFreeModule</b> function unmaps a file from system memory.


## -parameters




### -param h [in]

Handle to the memory-mapped file to be freed. This handle was obtained from <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564974">EngMapModule</a>
 

 

