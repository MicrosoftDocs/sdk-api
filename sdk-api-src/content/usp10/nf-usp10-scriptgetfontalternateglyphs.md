---
UID: NF:usp10.ScriptGetFontAlternateGlyphs
title: ScriptGetFontAlternateGlyphs function (usp10.h)
author: windows-sdk-content
description: Retrieves a list of alternate glyphs for a specified character that can be accessed through a specified OpenType feature.
old-location: intl\scriptgetfontalternateglyphs.htm
tech.root: Intl
ms.assetid: 2b64a14f-ad55-46df-a7a6-7f05fcb2c875
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ScriptGetFontAlternateGlyphs, ScriptGetFontAlternateGlyphs function [Internationalization for Windows Applications], _win32_ScriptGetFontAlternateGlyphs, intl.scriptgetfontalternateglyphs, usp10/ScriptGetFontAlternateGlyphs
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
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
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
 - ScriptGetFontAlternateGlyphs
product: Windows
targetos: Windows
req.typenames: 
req.redist: Usp10.dll version 1.600 or greater on Windows XP
ms.custom: 19H1
---

# ScriptGetFontAlternateGlyphs function


## -description


Retrieves a list of alternate glyphs for a specified character that can be accessed through a specified OpenType feature.


## -parameters




### -param hdc [in, optional]

Handle to the device context. For more information, see <a href="https://msdn.microsoft.com/c06c0eaf-41cb-4fd1-9750-a78355217f12">Caching</a>.


### -param psc [in, out]

Pointer to a <a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a> structure defining the script cache.


### -param psa [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a>. This parameter identifies the shaping engine, so that the array of alternate glyphs can be created with the correct scope.

Alternatively, the application can set this parameter to <b>NULL</b> to receive unfiltered results.


### -param tagScript [in]

An <a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a> structure defining the script tag associated with alternate glyphs.


### -param tagLangSys [in]

An <a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a> structure defining the language tag associated with alternate glyphs.


### -param tagFeature [in]

An <a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a> structure defining the feature tag associated with alternate glyphs.


### -param wGlyphId [in]

The identifier of the original glyph mapped from the character map table.


### -param cMaxAlternates [in]

Length of the array specified by <i>pAlternateGlyphs</i>.


### -param pAlternateGlyphs [out]

Pointer to buffer in which this function retrieves an array of glyph identifiers. The array includes the original glyph, followed by alternate glyphs. The first element is always the original glyph. Alternate forms are identified by an index into the array. The index is a value greater than one and less than the value of <i>pcAlternates</i>.

When the user chooses an alternate form from the user interface, the alternate glyph is applied to the corresponding character and the rendering is reformatted.


### -param pcAlternates [out]

Pointer to the number of elements in the array specified by <i>pAlternateGlyphs</i>.


## -returns



Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

If the number of alternate glyphs exceeds the value of <i>cMaxAlternates</i>, the function fails with E_OUTOFMEMORY. The application can try calling again with larger buffers.




## -remarks



When using alternate glyphs, the application first reshapes the original glyph without applying any feature tag, then selects an alternate. The original glyph is established as the base glyph. If another alternate is required, the original glyph provides information to match with the corresponding alternates list.

If an alternate glyph is used as the base glyph, no matching output list is found. The user interface uses the selected final form without providing the capability to choose another alternate.

The operations of <b>ScriptGetFontAlternateGlyphs</b> can be emulated by <a href="https://msdn.microsoft.com/1aecde5a-ddca-4163-9159-dafc15f9ca59">ScriptSubstituteSingleGlyph</a>. The application should try parameters one by one while glyphs are substituted.

For shaping fonts with Uniscribe, <a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a> is preferred over the older <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a> function.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c06c0eaf-41cb-4fd1-9750-a78355217f12">Caching</a>



<a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a>



<a href="https://msdn.microsoft.com/c673d5cc-c4ca-4238-8090-55abe3db324b">SCRIPT_ANALYSIS</a>



<a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a>



<a href="https://msdn.microsoft.com/da15d6b3-6725-43b8-9a2c-c19269a79d1e">ScriptItemizeOpenType</a>



<a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a>



<a href="https://msdn.microsoft.com/1aecde5a-ddca-4163-9159-dafc15f9ca59">ScriptSubstituteSingleGlyph</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

