---
UID: NF:imm.ImmSetCompositionFontW
title: ImmSetCompositionFontW function (imm.h)
author: windows-sdk-content
description: Sets the logical font to use to display characters in the composition window.
old-location: intl\immsetcompositionfont.htm
tech.root: Intl
ms.assetid: 5a3a9230-0ccf-4a6e-a3e0-7a3c7dbe35cf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImmSetCompositionFont, ImmSetCompositionFont function [Internationalization for Windows Applications], ImmSetCompositionFontA, ImmSetCompositionFontW, _win32_ImmSetCompositionFont, imm/ImmSetCompositionFont, imm/ImmSetCompositionFontA, imm/ImmSetCompositionFontW, intl.immsetcompositionfont
ms.topic: function
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmSetCompositionFontW (Unicode) and ImmSetCompositionFontA (ANSI)
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
 - ImmSetCompositionFont
 - ImmSetCompositionFontA
 - ImmSetCompositionFontW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmSetCompositionFontW function


## -description


Sets the logical font to use to display characters in the composition window.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param lplf [in]

Pointer to a <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure containing the font information to set.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function causes a <a href="https://msdn.microsoft.com/946bee83-91af-4647-9b22-96d42466352c">IMN_SETCOMPOSITIONFONT</a> command to be sent to an application. Even if the application never uses the composition window, it must set the appropriate font to ensure that characters are displayed properly. This is especially true for vertical writing.




## -see-also




<a href="https://msdn.microsoft.com/946bee83-91af-4647-9b22-96d42466352c">IMN_SETCOMPOSITIONFONT</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

