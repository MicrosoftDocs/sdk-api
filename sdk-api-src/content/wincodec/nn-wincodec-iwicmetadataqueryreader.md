---
UID: NN:wincodec.IWICMetadataQueryReader
title: IWICMetadataQueryReader
author: windows-sdk-content
description: Exposes methods for retrieving metadata blocks and items from a decoder or its image frames using a metadata query expression.
old-location: wic\_wic_codec_iwicmetadataqueryreader.htm
old-project: wic
ms.assetid: 588e00d2-e166-4ce5-bd8a-50ad0d5a3db9
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICMetadataQueryReader, IWICMetadataQueryReader interface [Windows Imaging Component], IWICMetadataQueryReader interface [Windows Imaging Component],described, _wic_codec_iwicmetadataqueryreader, wic._wic_codec_iwicmetadataqueryreader, wincodec/IWICMetadataQueryReader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICMetadataQueryReader
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataQueryReader interface


## -description


Exposes methods for retrieving metadata blocks and items from a decoder or its image frames using a metadata query expression.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataQueryReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICMetadataQueryReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataQueryReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f27c576a-3ff8-42bd-bad9-f7df18351a7f">GetContainerFormat</a>
</td>
<td align="left" width="63%">
Gets the metadata query readers container format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e9b0da5-90e3-4398-9113-0fb86a94cb0c">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of all metadata items at the current relative location within the metadata hierarchy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451128">GetLocation</a>
</td>
<td align="left" width="63%">
Retrieves the current path relative to the root metadata block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29d53a14-0509-4a96-9b8b-59952770559a">GetMetadataByName</a>
</td>
<td align="left" width="63%">
Retrieves the metadata block or item identified by a metadata query expression. 

</td>
</tr>
</table> 


## -remarks



A metadata query reader uses metadata query expressions to access embedded metadata. For more information on the metadata query language, see the <a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>.

The benefit of the query reader is the ability to access a metadata item in a single step.


The query reader also provides the way to traverse the whole set of metadata hierarchy with the help of the <a href="https://msdn.microsoft.com/8e9b0da5-90e3-4398-9113-0fb86a94cb0c">GetEnumerator</a> method.
However, it is not recommended to use this method since <a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a> and <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a> provide a more convenient and cheaper way.



#### Examples

The following code demonstrates how to obtain a query reader and use it to retrieve a metadata item.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode-&gt;GetMetadataQueryReader(&amp;pQueryReader);
}

if (SUCCEEDED(hr))
{
    hr = pQueryReader-&gt;GetMetadataByName(L"/app1/ifd/{ushort=18249}", &amp;value);
    PropVariantClear(&amp;value);
}</pre>
</td>
</tr>
</table></span></div>
The following code demonstrates how to obtain query reader and use it to retrieve a nested metadata block.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode-&gt;GetMetadataQueryReader(&amp;pQueryReader);
}

if (SUCCEEDED(hr))
{
    // Get the embedded IFD reader
    hr = pQueryReader-&gt;GetMetadataByName(L"/app1/ifd", &amp;value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal-&gt;QueryInterface(IID_IWICMetadataQueryReader, (void **)&amp;pEmbedReader);
    }
    PropVariantClear(&amp;value); // Clear value for new query
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

