---
UID: NF:immdev.ImmReleaseContext
title: ImmReleaseContext function (immdev.h)
author: windows-sdk-content
description: Releases the input context and unlocks the memory associated in the input context. An application must call this function for each call to the ImmGetContext function.
old-location: intl\immreleasecontext.htm
tech.root: Intl
ms.assetid: e14b087a-58ef-4360-9368-3fdd088c14f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImmReleaseContext, ImmReleaseContext function [Internationalization for Windows Applications], _win32_ImmReleaseContext, imm/ImmReleaseContext, intl.immreleasecontext
ms.topic: function
req.header: immdev.h
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
 - ImmReleaseContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmReleaseContext function


## -description


Releases the input context and unlocks the memory associated in the input context. An application must call this function for each call to the <a href="https://msdn.microsoft.com/2b7502ac-fa1e-4104-a7ad-051303131a73">ImmGetContext</a> function.


## -parameters




### -param HWND [in]

Handle to the window for which the input context was previously retrieved.


### -param HIMC [in]

Handle to the input context.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/2b7502ac-fa1e-4104-a7ad-051303131a73">ImmGetContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

