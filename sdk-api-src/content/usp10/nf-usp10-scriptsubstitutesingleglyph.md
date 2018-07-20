---
UID: NF:usp10.ScriptSubstituteSingleGlyph
title: ScriptSubstituteSingleGlyph function
author: windows-sdk-content
description: Enables substitution of a single glyph with one alternate form of the same glyph for OpenType processing.
old-location: intl\scriptsubstitutesingleglyph.htm
old-project: Intl
ms.assetid: 1aecde5a-ddca-4163-9159-dafc15f9ca59
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ScriptSubstituteSingleGlyph, ScriptSubstituteSingleGlyph function [Internationalization for Windows Applications], _win32_ScriptSubstituteSingleGlyph, intl.scriptsubstitutesingleglyph, usp10/ScriptSubstituteSingleGlyph
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
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptSubstituteSingleGlyph
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptSubstituteSingleGlyph function


## -description


Enables substitution of a single glyph with one alternate form of the same glyph for OpenType processing.


## -parameters




### -param hdc [in, optional]

Handle to the device context. For more information, see <a href="https://msdn.microsoft.com/c06c0eaf-41cb-4fd1-9750-a78355217f12">Caching</a>.


### -param psc [in, out]

Pointer to a <a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a> structure indicating the script cache.


### -param psa [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a>. This parameter identifies the shaping engine so that the correct substitute glyph is used.

Alternatively, the application can set this parameter to <b>NULL</b> to retrieve unfiltered results.


### -param tagScript [in]

An <a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a> structure defining the script tag for shaping.


### -param tagLangSys [in]

An <a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a> structure defining the language tag for shaping.


### -param tagFeature [in]

An <a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a> structure defining the feature tag to use for shaping the alternate glyph.


### -param lParameter [in]

Reference to the alternate glyph to substitute. This reference is an index to an array that contains all the alternate glyphs defined in the feature, as illustrated for <a href="https://msdn.microsoft.com/3f4d76f7-fd50-4a38-973b-329e477e5960">OPENTYPE_FEATURE_RECORD</a>. The alternate glyph array is one of the items retrieved by <a href="https://msdn.microsoft.com/2b64a14f-ad55-46df-a7a6-7f05fcb2c875">ScriptGetFontAlternateGlyphs</a>.


### -param wGlyphId [in]

Identifier of the original glyph.


### -param pwOutGlyphId [out]

Pointer to the location in which this function retrieves the identifier of the alternate glyph.


## -returns



Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



This function uses one-to-one substitution in which the application can substitute one glyph with one alternate form. Most often, applications use this function to set a bullet or an alternate glyph at the beginning or end of a line.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c06c0eaf-41cb-4fd1-9750-a78355217f12">Caching</a>



<a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a>



<a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a>



<a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a>



<a href="https://msdn.microsoft.com/2b64a14f-ad55-46df-a7a6-7f05fcb2c875">ScriptGetFontAlternateGlyphs</a>



<a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

