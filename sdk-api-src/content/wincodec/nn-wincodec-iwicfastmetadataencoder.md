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

# IWICFastMetadataEncoder interface


## -description


Exposes methods used for in-place metadata editing. A fast metadata encoder enables you to add and remove metadata to an image without having to fully re-encode the image.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICFastMetadataEncoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICFastMetadataEncoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICFastMetadataEncoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Finalizes metadata changes to the image stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d8a0993-101a-4aa5-9e2f-c3f95b9d3d3f">GetMetadataQueryWriter</a>
</td>
<td align="left" width="63%">
Retrieves a metadata query writer for fast metadata encoding.

</td>
</tr>
</table> 


## -remarks




            A decoder must be created using the <a href="https://msdn.microsoft.com/27b9d6e1-e171-4c7f-8f96-fa5a93923e35">WICDecodeOptions</a> value <b>WICDecodeMetadataCacheOnDemand</b> to perform in-place metadata updates. 
            Using the <b>WICDecodeMetadataCacheOnLoad</b> option causes the decoder to release the file stream necessary to perform the metadata updates. 
         


            Not all metadata formats support fast metadata encoding. The native metadata handlers that support metadata are IFD, Exif, XMP, and GPS.
         


            If a fast metadata encoder fails, the image will need to be fully re-encoded to add the metadata.
         


#### Examples

The following demonstrates how to obtain a fast metadata encoder from an image frame and use its query writer to write a metadata item.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IWICFastMetadataEncoder *pFME = NULL;
IWICMetadataQueryWriter *pFMEQW = NULL;

hr = pFactory-&gt;CreateFastMetadataEncoderFromFrameDecode(pFrameDecode, &amp;pFME);

if (SUCCEEDED(hr))
{
 	hr = pFME-&gt;GetMetadataQueryWriter(&amp;pFMEQW);
}

if (SUCCEEDED(hr))
{
	 // Add additional metadata
 	PROPVARIANT value;

	 PropVariantInit(&amp;value);

 	value.vt = VT_UI2;
	 value.uiVal = 99;
 	hr = pFMEQW-&gt;SetMetadataByName(L"/app1/ifd/{ushort=18249}", &amp;value);

 	PropVariantClear(&amp;value);
}

if (SUCCEEDED(hr))
{
	 hr = pFME-&gt;Commit();
}</pre>
</td>
</tr>
</table></span></div>


