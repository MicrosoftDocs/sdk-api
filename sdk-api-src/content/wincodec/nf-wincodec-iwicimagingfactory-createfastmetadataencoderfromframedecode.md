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

# IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode


## -description


Creates a new instance of the fast metadata encoder based on the given image frame.


## -parameters




### -param pIFrameDecoder [in]

Type: <b><a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a>*</b>

The <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a> to create the <a href="https://msdn.microsoft.com/c7b57a71-f1fe-4e30-a52e-72ab6ce021f7">IWICFastMetadataEncoder</a> from.


### -param ppIFastEncoder [out]

Type: <b><a href="https://msdn.microsoft.com/c7b57a71-f1fe-4e30-a52e-72ab6ce021f7">IWICFastMetadataEncoder</a>**</b>

When this method returns, contains a pointer to a new fast metadata encoder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a list of support metadata formats for fast metadata encoding, see <a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>.


#### Examples

The following code demonstrates how to use the <b>CreateFastMetadataEncoderFromFrameDecode</b> method for fast metadata encoding.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
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



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>



<a href="_wic_about_metadata.htm">Writing Metadata</a>
 

 

