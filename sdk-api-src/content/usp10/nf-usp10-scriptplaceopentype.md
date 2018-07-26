---
UID: NF:usp10.ScriptPlaceOpenType
title: ScriptPlaceOpenType function
author: windows-sdk-content
description: Generates glyphs and visual attributes for a Unicode run with OpenType information from the output of ScriptShapeOpenType.
old-location: intl\scriptplaceopentype.htm
old-project: Intl
ms.assetid: dd456988-ec9d-4e62-a93f-753ac08a18d9
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: ScriptPlaceOpenType, ScriptPlaceOpenType function [Internationalization for Windows Applications], _win32_ScriptPlaceOpenType, intl.scriptplaceopentype, usp10/ScriptPlaceOpenType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptPlaceOpenType
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptPlaceOpenType function


## -description


Generates <a href="uniscribe_glossary.htm">glyphs</a> and visual attributes for a Unicode run with OpenType information from the output of <a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a>.


## -parameters




### -param hdc [in, optional]

Handle to the device context. For more information, see <a href="https://msdn.microsoft.com/c06c0eaf-41cb-4fd1-9750-a78355217f12">Caching</a>.


### -param psc [in, out]

Pointer to a <a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a> structure identifying the script cache.


### -param psa [in, out]

Pointer to a <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a>. This structures identifies the shaping engine that governs the generated list of glyphs and their associated widths, and x and y placement offsets.

Alternatively, the application can set this parameter to <b>NULL</b> to receive unfiltered results.


### -param tagScript [in]

An <a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a> structure containing the OpenType script tag for the writing system to use.


### -param tagLangSys [in]

An <a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a> structure containing the OpenType language tag for the writing system.


### -param rcRangeChars [in, optional]

Array of the number of characters in each range. The number of members is indicated in the <i>cRanges</i> parameter. The total of values should equal the value of <i>cChars</i>.


### -param rpRangeProperties [in, optional]

Array of <a href="https://msdn.microsoft.com/f43a0873-f499-4d66-9fce-57f332c1dc77">TEXTRANGE_PROPERTIES</a> structures defining properties for each range. The number of elements is defined by the <i>cRanges</i> parameter.


### -param cRanges [in]

The number of OpenType feature ranges.


### -param pwcChars [in]

Pointer to an array of Unicode characters containing the run. The number of elements is defined by the <i>cRanges</i> parameter.


### -param pwLogClust [in]

Pointer to an array of logical cluster information. Each element in the array corresponds to a character in the array defined by <i>pwcChars</i>. The value of each element is the offset from the first glyph in the run to the first glyph in the cluster containing the corresponding character. Note that, when the <b>fRTL</b> member of the <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure is set to <b>TRUE</b>, the elements in <i>pwLogClust</i> decrease as the array is read.


### -param pCharProps [in]

Pointer to an array of character property values in the Unicode run.


### -param cChars [in]

Number of characters in the Unicode run.


### -param pwGlyphs [in]

Pointer to a glyph buffer obtained from an earlier call to the <a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a> function.


### -param pGlyphProps [in]

Pointer to an array of attributes for each of the glyphs to retrieve. The number of values equals the value of 
<i>cGlyphs</i>. Since there is one glyph property per glyph, this parameter has the number of elements indicated by <i>cGlyphs</i>.


### -param cGlyphs [in]

Count of glyphs in a glyph array buffer.


### -param piAdvance [out]

Pointer to an array, of length indicated by <i>cGlyphs</i>, in which this function retrieves <a href="uniscribe_glossary.htm">advance width</a> information.


### -param pGoffset [out]

Pointer to an array of <a href="https://msdn.microsoft.com/63fa8741-c8c8-480d-9702-2f4eb13bc01c">GOFFSET</a> structures in which this structure retrieves the x and y offsets of combining glyphs. This array must be of length indicated by <i>cGlyphs</i>.


### -param pABC [out, optional]

Pointer to an <a href="https://msdn.microsoft.com/00000000-0000-0000-0000-000000000001">ABC</a> structure in which this function retrieves the <a href="uniscribe_glossary.htm">ABC width</a> for the entire <a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">run</a>.


## -returns



Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. In all error cases, the output values are undefined. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

The function returns E_OUTOFMEMORY if the output buffer length indicated by <i>cGlyphs</i> is too small. The application can try calling again with larger buffers.

The function returns E_PENDING if the script cache specified by the <i>psc</i> parameter does not contain enough information to place the glyphs, and the <i>hdc</i> parameter is passed as <b>NULL</b> so that the function is unable to complete the placement process. The application should set up a correct device context for the run, and call this function again with the appropriate value in <i>hdc</i> and with all other parameters the same.




## -remarks



This function is preferred over the older <a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a> function. Some advantages of <b>ScriptPlaceOpenType</b> include the following:

<ul>
<li>Parameters directly correspond to OpenType tags in font layout tables.</li>
<li>Parameters define features applied to each character. Input is divided into ranges, and each range has OpenType properties associated with it.</li>
</ul>
The composite ABC width for the whole item identifies how much the glyphs <a href="uniscribe_glossary.htm">overhang</a> to the left of the start position and to the right of the length implied by the sum of the advance widths. The total advance width of the line is exactly abcA+abcB+abcC. The abcA and abcC values are maintained as proportions of the cell height represented in 8 bits and are thus roughly +/-1 percent. The total width retrieved, which is the sum of the abcA+abcB+abcC values indicated by <i>piAdvance</i>, is accurate to the resolution of the TrueType shaping engine.

All arrays are in visual order unless the <b>fLogicalOrder</b> member is set in the <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure indicated by the <i>psa</i> parameter.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a>



<a href="https://msdn.microsoft.com/63fa8741-c8c8-480d-9702-2f4eb13bc01c">GOFFSET</a>



<a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a>



<a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a>



<a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a>



<a href="https://msdn.microsoft.com/2f3a4d8d-c7b1-4005-aebb-d3e9f2e3a37f">SCRIPT_CHARPROP</a>



<a href="https://msdn.microsoft.com/5d68c8b6-77dd-48f7-b05a-0c02c9271097">SCRIPT_GLYPHPROP</a>



<a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a>



<a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>



<a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a>



<a href="https://msdn.microsoft.com/f43a0873-f499-4d66-9fce-57f332c1dc77">TEXTRANGE_PROPERTIES</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

