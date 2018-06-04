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

# IMFMetadataProvider::GetMFMetadata


## -description



          Gets a collection of metadata, either for an entire presentation, or for one stream in the presentation.


## -parameters




### -param pPresentationDescriptor [in]


            Pointer to the <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface of the media source's presentation descriptor.
          


### -param dwStreamIdentifier [in]


            If this parameter is zero, the method retrieves metadata that applies to the entire presentation. Otherwise, this <i></i> parameter specifies a stream identifier, and the method retrieves metadata for that stream. To get the stream identifier for a stream, call <a href="https://msdn.microsoft.com/d282ee48-6145-4557-8fa7-786b893327fa">IMFStreamDescriptor::GetStreamIdentifier</a>.
          


### -param dwFlags [in]


            Reserved. Must be zero.
          


### -param ppMFMetadata [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a> interface. Use this interface to access the metadata. The caller must release the interface.


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
<dt><b>MF_E_PROPERTY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No metadata is available for the requested stream or presentation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f32e78c9-a567-448d-947d-d7ea996bba5e">IMFMetadataProvider</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>
 

 

