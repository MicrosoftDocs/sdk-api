---
UID: NN:mfobjects.IMFMediaType
title: IMFMediaType (mfobjects.h)
author: windows-sdk-content
description: Represents a description of a media format.
old-location: mf\imfmediatype.htm
tech.root: medfound
ms.assetid: f1d60bec-71e4-4fcc-a020-92754b6f3c02
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaType, IMFMediaType interface [Media Foundation], IMFMediaType interface [Media Foundation],described, f1d60bec-71e4-4fcc-a020-92754b6f3c02, mf.imfmediatype, mfobjects/IMFMediaType
ms.topic: interface
f1_keywords: 
 - "mfobjects/IMFMediaType"
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMFMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaType interface


## -description


Represents a description of a media format.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaType</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFMediaType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-freerepresentation">FreeRepresentation</a>
</td>
<td align="left" width="63%">
Frees memory that was allocated by the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation">GetRepresentation</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype">GetMajorType</a>
</td>
<td align="left" width="63%">
Retrieves the major type of the format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation">GetRepresentation</a>
</td>
<td align="left" width="63%">
Retrieves an alternative representation of the media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-iscompressedformat">IsCompressedFormat</a>
</td>
<td align="left" width="63%">
Queries whether the media type is a compressed format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-isequal">IsEqual</a>
</td>
<td align="left" width="63%">
Compares two media types and determines whether they are identical.

</td>
</tr>
</table> 


## -remarks



To create a new media type, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>.
      

All of the information in a media type is stored as attributes. To clone a media type, call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems">IMFAttributes::CopyAllItems</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-type-attributes">Media Type Attributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-types">Media Types</a>
 

 

