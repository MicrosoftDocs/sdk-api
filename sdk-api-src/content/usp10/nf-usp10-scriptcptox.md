---
UID: NF:usp10.ScriptCPtoX
title: ScriptCPtoX function
author: windows-sdk-content
description: Generates the x offset from the left end or leading edge of a run to either the leading or trailing edge of a logical character cluster.
old-location: intl\scriptcptox.htm
tech.root: Intl
ms.assetid: 65a11b21-3f4b-463a-b347-a00add32380c
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: ScriptCPtoX, ScriptCPtoX function [Internationalization for Windows Applications], _win32_ScriptCPtoX, intl.scriptcptox, usp10/ScriptCPtoX
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
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptCPtoX
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
---

# ScriptCPtoX function


## -description


Generates the x offset from the left end or leading edge of a run to either the leading or trailing edge of a logical character <a href="uniscribe_glossary.htm">cluster</a>.


## -parameters




### -param iCP [in]

Logical character position in the run. This parameter corresponds to the offset of any logical character in the cluster.


### -param fTrailing [in]

<b>TRUE</b> to use the trailing edge of the logical character cluster to compute the offset. This parameter is set to <b>FALSE</b> to use the leading edge of the logical character cluster.


### -param cChars [in]

Number of characters in the run.


### -param cGlyphs [in]

Number of glyphs in the run.


### -param pwLogClust [in]

Pointer to the logical clusters.


### -param psva [in]

Pointer to a <a href="https://msdn.microsoft.com/83b77f60-2520-49ee-bc7f-27cb3db02ac8">SCRIPT_VISATTR</a> array of visual attributes.


### -param piAdvance [in]

Pointer to an advance widths value.


### -param psa [in]

Pointer to a <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure. The <b>fLogicalOrder</b> member specifies the end of the run from which to measure the offset. If the flag is set, the leading edge of the run is used. If the flag is not set, the left end of the run is used.


### -param piX [out]

Pointer to the buffer in which the function retrieves the x position of the caret.


## -returns



Returns 0 if successful. This function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



The leading or trailing edge of the character and the leading edge of a run depend on the direction of text in the run.

For scripts in which the caret is conventionally placed in the middle of clusters (for example, Arabic and Hebrew), the retrieved x position of the carat can be an interpolated position for any code point in the line.

For scripts in which the caret is conventionally snapped to the boundaries of clusters (for example, Thai and Indian), the x position is snapped to the requested edge of the cluster containing the logical character position indicated by <i>iCP</i>.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a>



<a href="https://msdn.microsoft.com/83b77f60-2520-49ee-bc7f-27cb3db02ac8">SCRIPT_VISATTR</a>



<a href="https://msdn.microsoft.com/98548d60-4cbd-4808-8027-1d8058c41d6d">ScriptXtoCP</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

