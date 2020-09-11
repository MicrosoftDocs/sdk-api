---
UID: NN:wmcontainer.IMFASFContentInfo
title: IMFASFContentInfo (wmcontainer.h)
description: Provides methods to work with the header section of files conforming to the Advanced Systems Format (ASF) specification.
helpviewer_keywords: ["9f490e6a-f378-45c1-a69d-985c6e884358","IMFASFContentInfo","IMFASFContentInfo interface [Media Foundation]","IMFASFContentInfo interface [Media Foundation]","described","mf.imfasfcontentinfo","wmcontainer/IMFASFContentInfo"]
old-location: mf\imfasfcontentinfo.htm
tech.root: mf
ms.assetid: 9f490e6a-f378-45c1-a69d-985c6e884358
ms.date: 12/05/2018
ms.keywords: 9f490e6a-f378-45c1-a69d-985c6e884358, IMFASFContentInfo, IMFASFContentInfo interface [Media Foundation], IMFASFContentInfo interface [Media Foundation],described, mf.imfasfcontentinfo, wmcontainer/IMFASFContentInfo
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFContentInfo
 - wmcontainer/IMFASFContentInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFContentInfo
---

# IMFASFContentInfo interface


## -description

Provides methods to work with the header section of files conforming to the Advanced Systems Format (ASF) specification. 

The <a href="https://docs.microsoft.com/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo Object</a> exposes this interface. To create the get a pointer to the <b>IMFASFContentInfo</b> interface, call <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo">MFCreateASFContentInfo</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFContentInfo</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFASFContentInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFContentInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader">GenerateHeader</a>
</td>
<td align="left" width="63%">
Encodes the data in the ASF ContentInfo object into a binary ASF header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor">GeneratePresentationDescriptor</a>
</td>
<td align="left" width="63%">
Creates a presentation descriptor for the ASF content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore">GetEncodingConfigurationPropertyStore</a>
</td>
<td align="left" width="63%">
Retrieves a property store that can be used to set encoding properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize">GetHeaderSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the header section of an ASF file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile">GetProfile</a>
</td>
<td align="left" width="63%">
Retrieves an ASF profile that describes the ASF content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader">ParseHeader</a>
</td>
<td align="left" width="63%">
Parses the information in an ASF header and uses that information to set values in the ContentInfo object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile">SetProfile</a>
</td>
<td align="left" width="63%">
Uses profile data from a profile object to configure settings in the ContentInfo object

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

