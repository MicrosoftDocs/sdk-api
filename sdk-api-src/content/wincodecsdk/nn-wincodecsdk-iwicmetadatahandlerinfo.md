---
UID: NN:wincodecsdk.IWICMetadataHandlerInfo
title: IWICMetadataHandlerInfo (wincodecsdk.h)
author: windows-sdk-content
description: Exposes methods that provide basic information about the registered metadata handler.
old-location: wic\_wic_codec_iwicmetadatahandlerinfo.htm
tech.root: wic
ms.assetid: 505105c2-de50-4b5f-9089-e9a3cea2f464
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICMetadataHandlerInfo, IWICMetadataHandlerInfo interface [Windows Imaging Component], IWICMetadataHandlerInfo interface [Windows Imaging Component],described, _wic_codec_iwicmetadatahandlerinfo, wic._wic_codec_iwicmetadatahandlerinfo, wincodecsdk/IWICMetadataHandlerInfo
ms.topic: interface
f1_keywords: 
 - "wincodecsdk/IWICMetadataHandlerInfo"
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
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
 - IWICMetadataHandlerInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataHandlerInfo interface


## -description


Exposes methods that provide basic information about the registered metadata handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataHandlerInfo</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccomponentinfo">IWICComponentInfo</a>. <b>IWICMetadataHandlerInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataHandlerInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatahandlerinfo-doesrequirefixedsize">DoesRequireFixedSize</a>
</td>
<td align="left" width="63%">
Determines if the metadata handler requires a fixed size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatahandlerinfo-doesrequirefullstream">DoesRequireFullStream</a>
</td>
<td align="left" width="63%">
Determines if the handler requires a full stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatahandlerinfo-doessupportpadding">DoesSupportPadding</a>
</td>
<td align="left" width="63%">
Determines if the metadata handler supports padding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatahandlerinfo-getcontainerformats">GetContainerFormats</a>
</td>
<td align="left" width="63%">
Retrieves the container formats supported by the metadata handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatahandlerinfo-getdevicemanufacturer">GetDeviceManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the device manufacturer of the metadata handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatahandlerinfo-getdevicemodels">GetDeviceModels</a>
</td>
<td align="left" width="63%">
Retrieves the device models that support the metadata handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatahandlerinfo-getmetadataformat">GetMetadataFormat</a>
</td>
<td align="left" width="63%">
Retrieves the metadata format of the metadata handler.

</td>
</tr>
</table> 

