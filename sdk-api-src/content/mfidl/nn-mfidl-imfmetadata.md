---
UID: NN:mfidl.IMFMetadata
title: IMFMetadata (mfidl.h)
description: Manages metadata for an object.helpviewer_keywords: ["411658ca-dc5e-445b-8d61-0c0429fcfbb1","IMFMetadata","IMFMetadata interface [Media Foundation]","IMFMetadata interface [Media Foundation]","described","mf.imfmetadata","mfidl/IMFMetadata"]
old-location: mf\imfmetadata.htm
tech.root: medfound
ms.assetid: 411658ca-dc5e-445b-8d61-0c0429fcfbb1
ms.date: 12/05/2018
ms.keywords: 411658ca-dc5e-445b-8d61-0c0429fcfbb1, IMFMetadata, IMFMetadata interface [Media Foundation], IMFMetadata interface [Media Foundation],described, mf.imfmetadata, mfidl/IMFMetadata
f1_keywords:
- mfidl/IMFMetadata
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMetadata interface


## -description


Manages metadata for an object. Metadata is information that describes a media file, stream, or other content. Metadata consists of individual properties, where each property contains a descriptive name and a value. A property may be associated with a particular language.

To get this interface from a media source, use the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider">IMFMetadataProvider</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMetadata</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMetadata</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-deleteproperty">DeleteProperty</a>
</td>
<td align="left" width="63%">
Deletes a metadata property.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages">GetAllLanguages</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the languages in which metadata is available.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames">GetAllPropertyNames</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the metadata property names on this object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getlanguage">GetLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the current language setting.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a metadata property.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage">SetLanguage</a>
</td>
<td align="left" width="63%">
Sets the language for setting and retrieving metadata.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of a metadata property.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider">IMFMetadataProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-metadata">Media Metadata</a>
 

 

