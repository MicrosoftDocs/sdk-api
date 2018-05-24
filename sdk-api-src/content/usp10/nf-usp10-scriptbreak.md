---
UID: NF:usp10.ScriptBreak
title: ScriptBreak function
author: windows-driver-content
description: Retrieves information for determining line breaks.
old-location: intl\scriptbreak.htm
old-project: Intl
ms.assetid: 1613819f-9473-4d9f-8a65-a109c9ef3f43
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: ScriptBreak, ScriptBreak function [Internationalization for Windows Applications], _win32_ScriptBreak, intl.scriptbreak, usp10/ScriptBreak
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: usp10.h
req.include-header: 
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
req.typenames: SCRIPT_JUSTIFY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	usp10.dll
-	Ext-MS-Win-usp10-l1-1-0.dll
-	GDI32.dll
-	GDI32Full.dll
api_name:
-	ScriptBreak
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptBreak function


## -description


Retrieves information for determining line breaks.


## -parameters




### -param pwcChars [in]

Pointer to the Unicode characters to process.


### -param cChars [in]

Number of Unicode characters to process.


### -param psa [in]

Pointer to the <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure obtained from an earlier call to <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>.


### -param psla [out]

Pointer to a buffer in which this function retrieves the character attributes as a <a href="https://msdn.microsoft.com/24131b04-870a-4841-b9cd-7a09497bd2e6">SCRIPT_LOGATTR</a> structure.


## -returns



Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



See <a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

This function does not require a device context and does not perform glyph shaping.

This function retrieves cursor movement and formatting break positions for an item in an array of <a href="https://msdn.microsoft.com/24131b04-870a-4841-b9cd-7a09497bd2e6">SCRIPT_LOGATTR</a> structures. To support mixed formatting within a single word correctly, the call to <b>ScriptBreak</b> should pass whole items as retrieved by <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>, and not the finer formatting runs.

The <a href="https://msdn.microsoft.com/24131b04-870a-4841-b9cd-7a09497bd2e6">SCRIPT_LOGATTR</a> structure identifies valid caret positions and line breaks. The <b>fCharStop</b> member specifies a flag that marks cluster boundaries for scripts that are conventionally restricted from moving inside clusters. The same boundaries can also be inferred by inspecting the logical cluster information retrieved by <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>. However, <b>ScriptBreak</b> is considerably faster in implementation and does not require a device context to be prepared.

The flags designated by the <b>fWordStop</b>, <b>fSoftBreak</b>, and <b>fWhiteSpace</b> members of <a href="https://msdn.microsoft.com/24131b04-870a-4841-b9cd-7a09497bd2e6">SCRIPT_LOGATTR</a> are only available through <b>ScriptBreak</b>.

Most shaping engines that identify invalid sequences set the flag indicated by the <b>fInvalid</b> member of <a href="https://msdn.microsoft.com/24131b04-870a-4841-b9cd-7a09497bd2e6">SCRIPT_LOGATTR</a> in <b>ScriptBreak</b>. The <b>fInvalidLogAttr</b> member of <a href="https://msdn.microsoft.com/473c1265-1c2c-48f3-a852-c701bebcf9eb">SCRIPT_PROPERTIES</a> identifies the applicable scripts.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a>



<a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a>



<a href="https://msdn.microsoft.com/24131b04-870a-4841-b9cd-7a09497bd2e6">SCRIPT_LOGATTR</a>



<a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>



<a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

