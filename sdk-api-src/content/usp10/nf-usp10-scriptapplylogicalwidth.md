---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ScriptApplyLogicalWidth function


## -description


Takes an array of advance widths for a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">run</a> and generates an array of adjusted advance glyph widths.


## -parameters




### -param piDx [in]

Pointer to an array of <a href="uniscribe_glossary.htm">advance widths</a> in logical order, one per code point.


### -param cChars [in]

Count of the logical code points in the run.


### -param cGlyphs [in]

Glyph count.


### -param pwLogClust [in]

Pointer to an array of logical clusters from <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>.


### -param psva [in]

Pointer to a <a href="https://msdn.microsoft.com/83b77f60-2520-49ee-bc7f-27cb3db02ac8">SCRIPT_VISATTR</a> structure from <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a> and updated by <a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>.


### -param piAdvance [in]

Pointer to an array of glyph advance widths from <a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>.


### -param psa [in]

Pointer to a <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure from <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a> and updated by <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a> and <a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>.


### -param pABC [in, out, optional]

Pointer to the overall <a href="uniscribe_glossary.htm">ABC width</a> of a run. On input, the parameter should contain the run ABC widths retrieved by <a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>. On output, the parameter indicates the ABC width updated to match the new widths.


### -param piJustify [out]

Pointer to an array in which the function retrieves the glyph advance widths. This array is suitable for passing to the <i>piJustify</i> parameter of <a href="https://msdn.microsoft.com/8d69caeb-4c02-4a9f-9dd5-ac3c13561a57">ScriptTextOut</a>.


## -returns



Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



This function can be used to reapply logical widths obtained with <a href="https://msdn.microsoft.com/ecedd0a1-aad8-4527-be46-6f7dd26a9e9b">ScriptGetLogicalWidths</a>. It can be useful in situations such as metafiling, for which advance width information must be recorded and reapplied in a font-independent manner, independent of glyph substitutions, such as ligaturization.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a>



<a href="https://msdn.microsoft.com/83b77f60-2520-49ee-bc7f-27cb3db02ac8">SCRIPT_VISATTR</a>



<a href="https://msdn.microsoft.com/ecedd0a1-aad8-4527-be46-6f7dd26a9e9b">ScriptGetLogicalWidths</a>



<a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>



<a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>



<a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a>



<a href="https://msdn.microsoft.com/8d69caeb-4c02-4a9f-9dd5-ac3c13561a57">ScriptTextOut</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

