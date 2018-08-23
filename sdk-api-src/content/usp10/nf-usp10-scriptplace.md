---
UID: NF:usp10.ScriptPlace
title: ScriptPlace function
author: windows-sdk-content
description: Generates glyph advance width and two-dimensional offset information from the output of ScriptShape.
old-location: intl\scriptplace.htm
old-project: Intl
ms.assetid: 7f88432f-052f-4781-8346-31c8a0771e51
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: ScriptPlace, ScriptPlace function [Internationalization for Windows Applications], _win32_ScriptPlace, intl.scriptplace, usp10/ScriptPlace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: usp10.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SCRIPT_JUSTIFY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptPlace
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptPlace function


## -description


Generates glyph <a href="https://msdn.microsoft.com/en-us/library/Dd374094(v=VS.85).aspx">advance width</a> and two-dimensional offset information from the output of <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>.


## -parameters




### -param hdc [in]

Optional. Handle to the device context. For more information, see <a href="https://msdn.microsoft.com/c06c0eaf-41cb-4fd1-9750-a78355217f12">Caching</a>.


### -param psc [in, out]

Pointer to a <a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a> structure identifying the script cache.


### -param pwGlyphs [in]

Pointer to a glyph buffer obtained from an earlier call to the <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a> function.


### -param cGlyphs [in]

Count of glyphs in the glyph buffer.


### -param psva [in]

Pointer to an array of <a href="https://msdn.microsoft.com/83b77f60-2520-49ee-bc7f-27cb3db02ac8">SCRIPT_VISATTR</a> structures indicating visual attributes.


### -param psa [in, out]

Pointer to a <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure. On input, this structure is obtained from a previous call to <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>. On output, this structure contains values retrieved by <b>ScriptPlace</b>.


### -param piAdvance [out]

Pointer to an array in which this function retrieves advance width information.


### -param pGoffset [out]

Optional. Pointer to an array of <a href="https://msdn.microsoft.com/63fa8741-c8c8-480d-9702-2f4eb13bc01c">GOFFSET</a> structures in which this function retrieves the x and y offsets of combining glyphs. This array must be of length indicated by <i>cGlyphs</i>.


### -param pABC [out]

Pointer to an <a href="https://msdn.microsoft.com/00000000-0000-0000-0000-000000000001">ABC</a> structure in which this function retrieves the <a href="https://msdn.microsoft.com/en-us/library/Dd374094(v=VS.85).aspx">ABC width</a> for the entire <a href="https://msdn.microsoft.com/en-us/library/Dd374094(v=VS.85).aspx">run</a>.


## -returns



Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

The function returns E_PENDING if the script cache specified by the <i>psc</i> parameter does not contain enough information to place the glyphs, and the <i>hdc</i> parameter is set to <b>NULL</b> so that the function cannot complete the placement process. The application should set up a correct device context for the run, and call this function again with the appropriate device context and with all other parameters the same.




## -remarks



See <a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

The composite ABC width for the whole item identifies how much the glyphs <a href="https://msdn.microsoft.com/en-us/library/Dd374094(v=VS.85).aspx">overhang</a> to the left of the start position and to the right of the length implied by the sum of the advance widths. The total advance width of the line is exactly abcA+abcB+abcC. The abcA and abcC values are maintained as proportions of the cell height represented in 8 bits and are thus roughly +/-1 percent. The total width retrieved, which is the sum of the abcA+abcB+abcC values indicated by <i>piAdvance</i>, is accurate to the resolution of the TrueType shaping engine.

All arrays are in visual order unless the <b>fLogicalOrder</b> member is set in the <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure indicated by the <i>psa</i> parameter.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a>



<a href="https://msdn.microsoft.com/63fa8741-c8c8-480d-9702-2f4eb13bc01c">GOFFSET</a>



<a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a>



<a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a>



<a href="https://msdn.microsoft.com/83b77f60-2520-49ee-bc7f-27cb3db02ac8">SCRIPT_VISATTR</a>



<a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>



<a href="https://msdn.microsoft.com/dd456988-ec9d-4e62-a93f-753ac08a18d9">ScriptPlaceOpenType</a>



<a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

