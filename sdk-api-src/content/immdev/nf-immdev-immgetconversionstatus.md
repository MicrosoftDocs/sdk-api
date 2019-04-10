---
UID: NF:immdev.ImmGetConversionStatus
title: ImmGetConversionStatus function (immdev.h)
author: windows-sdk-content
description: Retrieves the current conversion status.
old-location: intl\immgetconversionstatus.htm
tech.root: Intl
ms.assetid: 64220427-e352-4445-9476-35e6246e59cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImmGetConversionStatus, ImmGetConversionStatus function [Internationalization for Windows Applications], _win32_ImmGetConversionStatus, imm/ImmGetConversionStatus, intl.immgetconversionstatus
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
 - ImmGetConversionStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmGetConversionStatus function


## -description


Retrieves the current conversion status.


## -parameters




### -param HIMC [in]

Handle to the input context for which to retrieve status information.


### -param lpfdwConversion [out, optional]

Pointer to a variable in which the function retrieves a combination of conversion mode values. For more information, see <a href="https://msdn.microsoft.com/0b0afb4e-f7aa-4ca6-9174-21983b2a422b">IME Conversion Mode Values</a>.


### -param lpfdwSentence [out, optional]

Pointer to a variable in which the function retrieves a sentence mode value. For more information, see <a href="https://msdn.microsoft.com/24b12936-7dfc-4c8d-970c-d8354ad46d1d">IME Sentence Mode Values</a>.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



Conversion and sentence mode values are set only if the IME supports those modes.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

