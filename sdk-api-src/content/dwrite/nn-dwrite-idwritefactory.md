---
UID: NN:dwrite.IDWriteFactory
title: IDWriteFactory
author: windows-sdk-content
description: Used to create all subsequent DirectWrite objects. This interface is the root factory interface for all DirectWrite objects.
old-location: directwrite\IDWriteFactory.htm
tech.root: DirectWrite
ms.assetid: 73a85977-5c24-4abc-ad8c-1d0d6474bd7e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteFactory, IDWriteFactory interface [Direct Write], IDWriteFactory interface [Direct Write],described, directwrite.IDWriteFactory, dwrite/IDWriteFactory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory interface


## -description


Used to create all subsequent DirectWrite objects. This interface is the root factory interface for all DirectWrite objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/983864bc-b737-4a4d-8f3f-f062eb88cfa7">CreateCustomFontCollection</a>
</td>
<td align="left" width="63%">
 Creates a font collection using a custom font collection loader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c82ffcd-3e43-47cd-9a6c-ff8bd1d2625f">CreateCustomFontFileReference</a>
</td>
<td align="left" width="63%">
 Creates a reference to an application-specific font file resource.
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bfba2c4-755e-4bcf-82e7-610fc6b30be4">CreateCustomRenderingParams</a>
</td>
<td align="left" width="63%">
Creates a rendering parameters object with the specified properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b416d9f7-d2ce-477c-bf03-b20da2a55bb6">CreateEllipsisTrimmingSign</a>
</td>
<td align="left" width="63%">
 Creates an inline object for trimming, using an ellipsis as the omission sign.
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb3cd53f-a2cf-472c-aee9-88ac553f0ed0">CreateFontFace</a>
</td>
<td align="left" width="63%">
 Creates an object that represents a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec67407d-e19b-4135-83ff-f3115e2da90c">CreateFontFileReference</a>
</td>
<td align="left" width="63%">
 Creates a font file reference object from a local font file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9205ce6-1586-461a-9c48-3f3f25780dd0">CreateGdiCompatibleTextLayout</a>
</td>
<td align="left" width="63%">
 Takes a string, format, and associated constraints,
     and produces an object representing the result, formatted for a particular display resolution
     and measuring mode. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcc6fe70-84ef-43ac-82ff-3f09d977220f">CreateGlyphRunAnalysis</a>
</td>
<td align="left" width="63%">
 Creates a glyph run analysis object, which encapsulates information
     used to render a glyph run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddb6839a-9033-423a-a3f0-9352ec03e440">CreateMonitorRenderingParams</a>
</td>
<td align="left" width="63%">
 Creates a rendering parameters object with default settings for the specified monitor.
    In most cases, this is the preferred way to create a rendering parameters object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2778bfd-c721-44e8-ac0a-79aaa2b323a8">CreateNumberSubstitution</a>
</td>
<td align="left" width="63%">
 Creates a number substitution object using a locale name,
     substitution method, and an indicator  whether to ignore user overrides (use NLS
     defaults for the given culture instead).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5e3e609-62ee-4a0a-aed1-591be852590e">CreateRenderingParams</a>
</td>
<td align="left" width="63%">
 Creates a rendering parameters object with default settings for the primary monitor.
    Different monitors may have different rendering parameters, for more information see the <a href="https://msdn.microsoft.com/62274126-49da-4166-8482-73aac2b29c26">How to Add Support for Multiple Monitors</a> topic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f786de4-9498-49ef-b884-7e5f69cefe4a">CreateTextAnalyzer</a>
</td>
<td align="left" width="63%">
 Returns an interface for performing text analysis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6e7caba-5cba-4b6e-b146-10aa6d21cac1">CreateTextFormat</a>
</td>
<td align="left" width="63%">
 Creates a text format object used for text layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f76f85df-112f-4bc3-b922-a0d7940d2954">CreateTextLayout</a>
</td>
<td align="left" width="63%">
 Takes a string, text format, and associated constraints,
     and produces an object that represents the fully analyzed
     and formatted result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef6d8289-3a8a-4ec1-89a8-b1b52e311d63">CreateTypography</a>
</td>
<td align="left" width="63%">
 Creates a typography object for use in a text layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ff7930b-8840-42d6-b52d-6766deab1aac">GetGdiInterop</a>
</td>
<td align="left" width="63%">
 Creates an object that is used for interoperability with GDI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f5cbea1-9775-4266-aa3c-7c15892d61b1">GetSystemFontCollection</a>
</td>
<td align="left" width="63%">
 Gets an object which represents the set of installed fonts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/495f8f56-42b6-4731-a26e-5da2c56a28ed">RegisterFontCollectionLoader</a>
</td>
<td align="left" width="63%">
Registers a custom font collection loader with the factory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5b28c3d-c3ad-4435-92c8-07841e8d160a">RegisterFontFileLoader</a>
</td>
<td align="left" width="63%">
 Registers a font file loader with DirectWrite.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a8682e3-72de-4afd-b9db-ba9b0d79f195">UnregisterFontCollectionLoader</a>
</td>
<td align="left" width="63%">
 Unregisters a custom font collection loader that was previously registered using <a href="https://msdn.microsoft.com/495f8f56-42b6-4731-a26e-5da2c56a28ed">RegisterFontCollectionLoader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f048671e-dfb6-449d-9bcd-e5df8408c01a">UnregisterFontFileLoader</a>
</td>
<td align="left" width="63%">
 Unregisters a font file loader that was previously registered with the DirectWrite font system using <a href="https://msdn.microsoft.com/f5b28c3d-c3ad-4435-92c8-07841e8d160a">RegisterFontFileLoader</a>.

</td>
</tr>
</table> 


## -remarks



Create an <b>IDWriteFactory</b> object by using the <a href="https://msdn.microsoft.com/c74c0906-0a5c-4ab8-87cf-a195566e1d9e">DWriteCreateFactory</a> function.  


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



