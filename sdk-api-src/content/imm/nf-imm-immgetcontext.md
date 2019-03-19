---
UID: NF:imm.ImmGetContext
title: ImmGetContext function (imm.h)
author: windows-sdk-content
description: Returns the input context associated with the specified window.
old-location: intl\immgetcontext.htm
tech.root: Intl
ms.assetid: 2b7502ac-fa1e-4104-a7ad-051303131a73
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImmGetContext, ImmGetContext function [Internationalization for Windows Applications], _win32_ImmGetContext, imm/ImmGetContext, intl.immgetcontext
ms.topic: function
req.header: imm.h
req.include-header: Immdev.h, Windows.h
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
 - ImmGetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmGetContext function


## -description


Returns the input context associated with the specified window.


## -parameters




### -param HWND [in]

Handle to the window for which to retrieve the input context.


## -returns



Returns the handle to the input context.




## -remarks



An application should routinely use this function to retrieve the current input context before attempting to access information in the context.

The application must call <a href="https://msdn.microsoft.com/e14b087a-58ef-4360-9368-3fdd088c14f6">ImmReleaseContext</a> when it is finished with the input context.




## -see-also




<a href="https://msdn.microsoft.com/e14b087a-58ef-4360-9368-3fdd088c14f6">ImmReleaseContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

