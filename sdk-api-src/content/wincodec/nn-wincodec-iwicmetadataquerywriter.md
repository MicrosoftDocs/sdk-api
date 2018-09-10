---
UID: NN:wincodec.IWICMetadataQueryWriter
title: IWICMetadataQueryWriter
author: windows-sdk-content
description: Exposes methods for setting or removing metadata blocks and items to an encoder or its image frames using a metadata query expression.
old-location: wic\_wic_codec_iwicmetadataquerywriter.htm
tech.root: wic
ms.assetid: 065cccc3-778f-42c4-823a-354b08bbd1f1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWICMetadataQueryWriter, IWICMetadataQueryWriter interface [Windows Imaging Component], IWICMetadataQueryWriter interface [Windows Imaging Component],described, _wic_codec_iwicmetadataquerywriter, wic._wic_codec_iwicmetadataquerywriter, wincodec/IWICMetadataQueryWriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICMetadataQueryWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICMetadataQueryWriter interface


## -description


Exposes methods for setting or removing metadata blocks and items to an encoder or its image frames using a metadata query expression.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataQueryWriter</b> interface inherits from <a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>. <b>IWICMetadataQueryWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataQueryWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/419d56db-42a6-4467-8ec5-7c7d2c5cdcf4">RemoveMetadataByName</a>
</td>
<td align="left" width="63%">
Removes a metadata item from a specific location using a metadata query expression.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd3a9752-f13f-4f19-b2bd-04b5df1e0dd2">SetMetadataByName</a>
</td>
<td align="left" width="63%">
Sets a metadata item to a specific location.

</td>
</tr>
</table> 


## -remarks



A metadata query writer uses metadata query expressions to set or remove metadata. For more information on the metadata query language, see the <a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>.


#### Examples

The following code demonstrates how to create an XMP query writer and add a new metadata item to it.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>// Create XMP block
IWICMetadataQueryWriter *pXMPWriter = NULL;

if (SUCCEEDED(hr))
{
    hr = pFactory-&gt;CreateQueryWriter(GUID_MetadataFormatXMP, NULL, &amp;pXMPWriter);
}

// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&amp;value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
	
    hr = pXMPWriter-&gt;SetMetadataByName(L"/dc:title", &amp;value);

    PropVariantClear(&amp;value);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a7cfaa6d-e17d-458a-ae63-72963615bef8">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

