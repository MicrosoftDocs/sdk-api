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

# IMFMediaType::GetRepresentation


## -description



Retrieves an alternative representation of the media type. Currently only the DirectShow <b>AM_MEDIA_TYPE</b> structure is supported.




## -parameters




### -param guidRepresentation [in]


            GUID that specifies the representation to retrieve. The following values are defined.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AM_MEDIA_TYPE_REPRESENTATION"></a><a id="am_media_type_representation"></a><dl>
<dt><b>AM_MEDIA_TYPE_REPRESENTATION</b></dt>
</dl>
</td>
<td width="60%">

                Convert the media type to a DirectShow <b>AM_MEDIA_TYPE</b> structure. The method selects the most appropriate format structure (<b>pbFormat</b>).
              

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MFVideoFormat"></a><a id="format_mfvideoformat"></a><a id="FORMAT_MFVIDEOFORMAT"></a><dl>
<dt><b>FORMAT_MFVideoFormat</b></dt>
</dl>
</td>
<td width="60%">

                Convert the media type to a DirectShow <b>AM_MEDIA_TYPE</b> structure with an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> format structure.
              

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_VideoInfo"></a><a id="format_videoinfo"></a><a id="FORMAT_VIDEOINFO"></a><dl>
<dt><b>FORMAT_VideoInfo</b></dt>
</dl>
</td>
<td width="60%">

                Convert the media type to a DirectShow <b>AM_MEDIA_TYPE</b> structure with a <b>VIDEOINFOHEADER</b> format structure.
              

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_VideoInfo2"></a><a id="format_videoinfo2"></a><a id="FORMAT_VIDEOINFO2"></a><dl>
<dt><b>FORMAT_VideoInfo2</b></dt>
</dl>
</td>
<td width="60%">

                Convert the media type to a DirectShow <b>AM_MEDIA_TYPE</b> structure with a <b>VIDEOINFOHEADER2</b> format structure.
              

</td>
</tr>
</table>
 


### -param ppvRepresentation [out]


            Receives a pointer to a structure that contains the representation. The method allocates the memory for the structure. The caller must release the memory by calling <a href="https://msdn.microsoft.com/d2007f16-543f-4f05-a44d-b4b4ae8019fb">IMFMediaType::FreeRepresentation</a>.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">

                The details of the media type do not match the requested representation.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">

                The media type is not valid.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_REPRESENTATION</b></dt>
</dl>
</td>
<td width="60%">

                The media type does not support the requested representation.
              

</td>
</tr>
</table>
 




## -remarks




        If you request a specific format structure in the <i>guidRepresentation</i> parameter, such as <b>VIDEOINFOHEADER</b>, you might lose some of the format information.
      


        You can also use the <a href="https://msdn.microsoft.com/dbb69578-2563-476f-92f4-6b4e2bb2c77a">MFInitAMMediaTypeFromMFMediaType</a> function to convert a Media Foundation media type into a DirectShow media type.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>



<a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

