---
UID: NF:imm.ImmSetConversionStatus
title: ImmSetConversionStatus function
author: windows-sdk-content
description: Sets the current conversion status.
old-location: intl\immsetconversionstatus.htm
tech.root: Intl
ms.assetid: cdf6ea84-bab9-4ecc-b2d1-748e5e28615f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ImmSetConversionStatus, ImmSetConversionStatus function [Internationalization for Windows Applications], _win32_ImmSetConversionStatus, imm/ImmSetConversionStatus, intl.immsetconversionstatus
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
 - ImmSetConversionStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmSetConversionStatus function


## -description


Sets the current conversion status.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param DWORD [in]

Conversion mode values. For more information, see <a href="https://msdn.microsoft.com/0b0afb4e-f7aa-4ca6-9174-21983b2a422b">IME Conversion Mode Values</a>.


#### - fdwSentence [in]

Sentence mode values. For more information, see <a href="https://msdn.microsoft.com/24b12936-7dfc-4c8d-970c-d8354ad46d1d">IME Sentence Mode Values</a>.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function sends the <a href="https://msdn.microsoft.com/62bb9717-cc41-4e34-af1a-ff41324bd3a9">IMN_SETCONVERSIONMODE</a> and <a href="https://msdn.microsoft.com/72455193-cd17-45f8-b19c-a1f735ff81bf">IMN_SETSENTENCEMODE</a> commands to the application.

<div class="alert"><b>Note</b>  <b>Beginning with Windows 8:</b> By default, the input switch is set per user instead of per thread. 
The Microsoft IME (Japanese) respects the mode globally, and therefore  <b>ImmSetConversionStatus</b> fails when getting focus.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/62bb9717-cc41-4e34-af1a-ff41324bd3a9">IMN_SETCONVERSIONMODE</a>



<a href="https://msdn.microsoft.com/72455193-cd17-45f8-b19c-a1f735ff81bf">IMN_SETSENTENCEMODE</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

