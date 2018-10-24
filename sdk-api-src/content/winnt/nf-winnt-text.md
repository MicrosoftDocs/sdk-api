---
UID: NF:winnt.TEXT
title: TEXT macro
author: windows-sdk-content
description: Identifies a string as Unicode when UNICODE is defined by a preprocessor directive during compilation. Otherwise, the macro identifies a string as an ANSI string.
old-location: intl\text.htm
tech.root: Intl
ms.assetid: 427d365f-2277-460c-8120-3ccb6c6cea4f
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: TEXT, TEXT macro [Internationalization for Windows Applications], _win32_TEXT_Macro, intl.text, winnt/TEXT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TEXT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TEXT macro


## -description


Identifies a string as Unicode when UNICODE is defined by a preprocessor directive during compilation. Otherwise, the macro identifies a string as an ANSI string.


## -parameters




### -param quote

Pointer to the string to interpret as UTF-16 or ANSI.


## -remarks



This macro interprets an ANSI string at runtime according to the current Windows ANSI code page. Literal ANSI strings that are not strictly ASCII are interpreted differently when processed with different Windows ANSI code pages. For example, "\0xC4" in code page 1252 (Latin-1) represents Upper Case A with Dieresis (Ä). However, in code page 1253 (Greek), the string represents Upper Case Delta (Δ). These different interpretations lead to development and maintenance issues. For example, a developer might correct a string when using a different system code page from the page used by the original developer; or a build computer might use a different code page. The different interpretations also pose runtime issues, for example, when the end user computer uses a different code page to interpret a string from that used by the build computer.




## -see-also




<a href="https://msdn.microsoft.com/dd4930db-229f-4917-b7ca-d619e7e4564d">Unicode and Character Set Macros</a>



<a href="https://msdn.microsoft.com/8c1c6582-b58c-4008-9ce5-208acc191d9f">Unicode and Character Sets</a>
 

 

