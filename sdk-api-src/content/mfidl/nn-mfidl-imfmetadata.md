---
UID: NN:mfidl.IMFMetadata
title: IMFMetadata
author: windows-sdk-content
description: Manages metadata for an object.
old-location: mf\imfmetadata.htm
tech.root: medfound
ms.assetid: 411658ca-dc5e-445b-8d61-0c0429fcfbb1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 411658ca-dc5e-445b-8d61-0c0429fcfbb1, IMFMetadata, IMFMetadata interface [Media Foundation], IMFMetadata interface [Media Foundation],described, mf.imfmetadata, mfidl/IMFMetadata
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMetadata interface


## -description


Manages metadata for an object. Metadata is information that describes a media file, stream, or other content. Metadata consists of individual properties, where each property contains a descriptive name and a value. A property may be associated with a particular language.

To get this interface from a media source, use the <a href="https://msdn.microsoft.com/f32e78c9-a567-448d-947d-d7ea996bba5e">IMFMetadataProvider</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMetadata</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMetadata</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMetadata</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c9a406d-6144-4e9c-b62c-1d9c691391f0">DeleteProperty</a>
</td>
<td align="left" width="63%">
Deletes a metadata property.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69296ec5-5811-4f0f-ae9c-cabca3e66158">GetAllLanguages</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the languages in which metadata is available.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0944d42-d6e6-420d-9980-ca6c62736b3d">GetAllPropertyNames</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the metadata property names on this object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75295c93-a389-42c4-aa56-debc36a5f532">GetLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the current language setting.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/177c8612-5c9f-4a71-9ee1-a4c67737af2d">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a metadata property.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da615053-ddd5-448e-905c-b060cdaefa95">SetLanguage</a>
</td>
<td align="left" width="63%">
Sets the language for setting and retrieving metadata.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/416a7fba-506c-405d-a230-7e8a1c801209">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of a metadata property.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f32e78c9-a567-448d-947d-d7ea996bba5e">IMFMetadataProvider</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>
 

 

