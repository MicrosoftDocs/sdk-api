---
UID: NF:imm.ImmDisableTextFrameService
title: ImmDisableTextFrameService function
author: windows-sdk-content
description: ImmDisableTextFrameService is no longer available for use as of Windows Vista.
old-location: intl\immdisabletextframeservice.htm
old-project: Intl
ms.assetid: ce294f9e-ba0b-460d-8685-85371af8a7e6
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ImmDisableTextFrameService, ImmDisableTextFrameService function [Internationalization for Windows Applications], _win32_ImmDisableTextFrameService, imm/ImmDisableTextFrameService, intl.immdisabletextframeservice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imm32.dll
api_name:
 - ImmDisableTextFrameService
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmDisableTextFrameService function


## -description


<p class="CCE_Message">[<b>ImmDisableTextFrameService</b> is no longer available for use as of Windows Vista. Instead, use <a href="https://msdn.microsoft.com/c563fc24-3c56-40ac-8539-8336d5231537">ImmDisableIME</a>.
]

Disables the text service for the specified thread. For details, see <a href="https://msdn.microsoft.com/ecc34b2e-89e8-48a8-8a8e-442d2145fe24">Text Services Framework</a> (TSF).
		


## -parameters




### -param idThread [in]

Identifier of the thread for which to disable the text service. The thread must be in the same process as the application. The application sets this parameter to 0 to disable the service for the current thread. The application sets the parameter to –1 to disable the service for all threads in the current process.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



An application calls this function if it has a thread that is incompatible with TSF.

Note that TSF functionality is provided to applications that are not specifically written to use TSF, Input Method Manager (IMM32), or Active Input Method Manager (AIMM 1.2). Although an application can be written to use TSF, IMM32, and AIMM 1.2, there can be specific controls within the application that do not use these technologies. TSF support is provided to these specific controls as well. This TSF feature is available beginning with Windows XP when all of these dynamic-link libraries (DLLs) are loaded: system modules User32.dll, Imm32.dll, and Win32k.sys, and TSF modules Msctf.dll and Msimtf.dll.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

