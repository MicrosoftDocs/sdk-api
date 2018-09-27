---
UID: NF:imm.ImmSetCompositionWindow
title: ImmSetCompositionWindow function
author: windows-sdk-content
description: Sets the position of the composition window.
old-location: intl\immsetcompositionwindow.htm
tech.root: Intl
ms.assetid: 01204f4c-4cf1-4bff-99db-fa0c66c2a8e9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ImmSetCompositionWindow, ImmSetCompositionWindow function [Internationalization for Windows Applications], _win32_ImmSetCompositionWindow, imm/ImmSetCompositionWindow, intl.immsetcompositionwindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imm32.dll
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmSetCompositionWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmSetCompositionWindow function


## -description


Sets the position of the composition window.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param lpCompForm [in]

Pointer to a <a href="https://msdn.microsoft.com/9b76474a-1ea9-4fcf-9fa8-deee5009a7ba">COMPOSITIONFORM</a> structure that contains the new position and other related information about the composition window.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function causes an <a href="https://msdn.microsoft.com/07a9f0f6-587e-47c6-8f18-b48bdab0a541">IMN_SETCOMPOSITIONWINDOW</a> command to be sent to the application.




## -see-also




<a href="https://msdn.microsoft.com/9b76474a-1ea9-4fcf-9fa8-deee5009a7ba">COMPOSITIONFORM</a>



<a href="https://msdn.microsoft.com/07a9f0f6-587e-47c6-8f18-b48bdab0a541">IMN_SETCOMPOSITIONWINDOW</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

