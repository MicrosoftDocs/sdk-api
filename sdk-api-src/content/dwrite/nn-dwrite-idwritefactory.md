---
UID: NN:dwrite.IDWriteFactory
title: IDWriteFactory (dwrite.h)
description: Used to create all subsequent DirectWrite objects. This interface is the root factory interface for all DirectWrite objects.
old-location: directwrite\IDWriteFactory.htm
tech.root: DirectWrite
ms.assetid: 73a85977-5c24-4abc-ad8c-1d0d6474bd7e
ms.date: 12/05/2018
ms.keywords: IDWriteFactory, IDWriteFactory interface [Direct Write], IDWriteFactory interface [Direct Write],described, directwrite.IDWriteFactory, dwrite/IDWriteFactory
ms.topic: interface
f1_keywords:
- dwrite/IDWriteFactory
dev_langs:
- c++
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory interface


## -description


Used to create all subsequent DirectWrite objects. This interface is the root factory interface for all DirectWrite objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection">CreateCustomFontCollection</a>
</td>
<td align="left" width="63%">
 Creates a font collection using a custom font collection loader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference">CreateCustomFontFileReference</a>
</td>
<td align="left" width="63%">
 Creates a reference to an application-specific font file resource.
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams">CreateCustomRenderingParams</a>
</td>
<td align="left" width="63%">
Creates a rendering parameters object with the specified properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createellipsistrimmingsign">CreateEllipsisTrimmingSign</a>
</td>
<td align="left" width="63%">
 Creates an inline object for trimming, using an ellipsis as the omission sign.
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontface">CreateFontFace</a>
</td>
<td align="left" width="63%">
 Creates an object that represents a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference">CreateFontFileReference</a>
</td>
<td align="left" width="63%">
 Creates a font file reference object from a local font file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-creategdicompatibletextlayout">CreateGdiCompatibleTextLayout</a>
</td>
<td align="left" width="63%">
 Takes a string, format, and associated constraints,
     and produces an object representing the result, formatted for a particular display resolution
     and measuring mode. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createglyphrunanalysis">CreateGlyphRunAnalysis</a>
</td>
<td align="left" width="63%">
 Creates a glyph run analysis object, which encapsulates information
     used to render a glyph run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams">CreateMonitorRenderingParams</a>
</td>
<td align="left" width="63%">
 Creates a rendering parameters object with default settings for the specified monitor.
    In most cases, this is the preferred way to create a rendering parameters object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createnumbersubstitution">CreateNumberSubstitution</a>
</td>
<td align="left" width="63%">
 Creates a number substitution object using a locale name,
     substitution method, and an indicator  whether to ignore user overrides (use NLS
     defaults for the given culture instead).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams">CreateRenderingParams</a>
</td>
<td align="left" width="63%">
 Creates a rendering parameters object with default settings for the primary monitor.
    Different monitors may have different rendering parameters, for more information see the <a href="/windows/win32/DirectWrite/how-to-add-support-for-multiple-monitors">How to Add Support for Multiple Monitors</a> topic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextanalyzer">CreateTextAnalyzer</a>
</td>
<td align="left" width="63%">
 Returns an interface for performing text analysis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat">CreateTextFormat</a>
</td>
<td align="left" width="63%">
 Creates a text format object used for text layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout">CreateTextLayout</a>
</td>
<td align="left" width="63%">
 Takes a string, text format, and associated constraints,
     and produces an object that represents the fully analyzed
     and formatted result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography">CreateTypography</a>
</td>
<td align="left" width="63%">
 Creates a typography object for use in a text layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop">GetGdiInterop</a>
</td>
<td align="left" width="63%">
 Creates an object that is used for interoperability with GDI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection">GetSystemFontCollection</a>
</td>
<td align="left" width="63%">
 Gets an object which represents the set of installed fonts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader">RegisterFontCollectionLoader</a>
</td>
<td align="left" width="63%">
Registers a custom font collection loader with the factory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader">RegisterFontFileLoader</a>
</td>
<td align="left" width="63%">
 Registers a font file loader with DirectWrite.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader">UnregisterFontCollectionLoader</a>
</td>
<td align="left" width="63%">
 Unregisters a custom font collection loader that was previously registered using <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader">RegisterFontCollectionLoader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader">UnregisterFontFileLoader</a>
</td>
<td align="left" width="63%">
 Unregisters a font file loader that was previously registered with the DirectWrite font system using <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader">RegisterFontFileLoader</a>.

</td>
</tr>
</table> 


## -remarks



Create an <b>IDWriteFactory</b> object by using the <a href="/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory">DWriteCreateFactory</a> function.  


```cpp

if (SUCCEEDED(hr))
{
    hr = DWriteCreateFactory(
        DWRITE_FACTORY_TYPE_SHARED,
        __uuidof(IDWriteFactory),
        reinterpret_cast<IUnknown**>(&pDWriteFactory_)
        );
}


```


An <b>IDWriteFactory</b> object holds state information, such as font loader registration and cached font data.  This state can be shared or isolated.  Shared is recommended for most applications because it saves memory.  However, isolated can be useful in situations where you want to have a separate state for some objects.



