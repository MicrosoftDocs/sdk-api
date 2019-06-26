---
UID: NF:immdev.ImmGetCompositionFontW
title: ImmGetCompositionFontW function (immdev.h)
author: windows-sdk-content
description: Retrieves information about the logical font currently used to display characters in the composition window.
old-location: intl\immgetcompositionfont.htm
tech.root: Intl
ms.assetid: c38f424f-84d4-4181-9ada-bbd178a70373
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImmGetCompositionFont, ImmGetCompositionFont function [Internationalization for Windows Applications], ImmGetCompositionFontA, ImmGetCompositionFontW, _win32_ImmGetCompositionFont, imm/ImmGetCompositionFont, imm/ImmGetCompositionFontA, imm/ImmGetCompositionFontW, intl.immgetcompositionfont
ms.topic: function
f1_keywords: 
 - "immdev/ImmGetCompositionFont"
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
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
ms.custom: 19H1
---

# ImmGetCompositionFontW function


## -description


Retrieves information about the logical font currently used to display characters in the composition window.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param lplf [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-taglogfonta">LOGFONT</a> structure in which this function retrieves the font information.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

