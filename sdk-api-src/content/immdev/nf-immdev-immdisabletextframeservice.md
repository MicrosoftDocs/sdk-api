---
UID: NF:immdev.ImmDisableTextFrameService
title: ImmDisableTextFrameService function (immdev.h)
description: The ImmDisableTextFrameService function (immdev.h) is no longer available for use as of Windows Vista.
helpviewer_keywords: ["ImmDisableTextFrameService","ImmDisableTextFrameService function [Internationalization for Windows Applications]","_win32_ImmDisableTextFrameService","imm/ImmDisableTextFrameService","intl.immdisabletextframeservice"]
old-location: intl\immdisabletextframeservice.htm
tech.root: Intl
ms.assetid: ce294f9e-ba0b-460d-8685-85371af8a7e6
ms.date: 08/04/2022
ms.keywords: ImmDisableTextFrameService, ImmDisableTextFrameService function [Internationalization for Windows Applications], _win32_ImmDisableTextFrameService, imm/ImmDisableTextFrameService, intl.immdisabletextframeservice
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
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
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmDisableTextFrameService
 - immdev/ImmDisableTextFrameService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imm32.dll
api_name:
 - ImmDisableTextFrameService
---

# ImmDisableTextFrameService function


## -description

<p class="CCE_Message">[<b>ImmDisableTextFrameService</b> is no longer available for use as of Windows Vista. Instead, use <a href="/windows/desktop/api/imm/nf-imm-immdisableime">ImmDisableIME</a>.
]

Disables the text service for the specified thread. For details, see <a href="/windows/desktop/TSF/text-services-framework">Text Services Framework</a> (TSF).

## -parameters

### -param idThread [in]

Identifier of the thread for which to disable the text service. The thread must be in the same process as the application. The application sets this parameter to 0 to disable the service for the current thread. The application sets the parameter to –1 to disable the service for all threads in the current process.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -remarks

An application calls this function if it has a thread that is incompatible with TSF.

Note that TSF functionality is provided to applications that are not specifically written to use TSF, Input Method Manager (IMM32), or Active Input Method Manager (AIMM 1.2). Although an application can be written to use TSF, IMM32, and AIMM 1.2, there can be specific controls within the application that do not use these technologies. TSF support is provided to these specific controls as well. This TSF feature is available beginning with Windows XP when all of these dynamic-link libraries (DLLs) are loaded: system modules User32.dll, Imm32.dll, and Win32k.sys, and TSF modules Msctf.dll and Msimtf.dll.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
