---
UID: NF:imm.ImmGetCompositionFontW
title: ImmGetCompositionFontW function
author: windows-sdk-content
description: Retrieves information about the logical font currently used to display characters in the composition window.
old-location: intl\immgetcompositionfont.htm
tech.root: Intl
ms.assetid: c38f424f-84d4-4181-9ada-bbd178a70373
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ImmGetCompositionFont, ImmGetCompositionFont function [Internationalization for Windows Applications], ImmGetCompositionFontA, ImmGetCompositionFontW, _win32_ImmGetCompositionFont, imm/ImmGetCompositionFont, imm/ImmGetCompositionFontA, imm/ImmGetCompositionFontW, intl.immgetcompositionfont
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
req.unicode-ansi: ImmGetCompositionFontW (Unicode) and ImmGetCompositionFontA (ANSI)
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
api_name:
 - ImmGetCompositionFont
 - ImmGetCompositionFontA
 - ImmGetCompositionFontW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ImmGetCompositionFontW
: 
---

# ImmGetCompositionFontW function


## -description


Retrieves information about the logical font currently used to display characters in the composition window.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param lplf [out]

Pointer to a <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure in which this function retrieves the font information.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

