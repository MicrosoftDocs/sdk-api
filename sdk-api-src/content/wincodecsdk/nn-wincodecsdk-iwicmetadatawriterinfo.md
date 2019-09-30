---
UID: NN:wincodecsdk.IWICMetadataWriterInfo
title: IWICMetadataWriterInfo (wincodecsdk.h)
author: windows-sdk-content
description: Exposes methods that provide basic information about the registered metadata writer.
old-location: wic\_wic_codec_iwicmetadatawriterinfo.htm
tech.root: wic
ms.assetid: 467200e7-9b08-4372-9a01-660e56a15bfe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICMetadataWriterInfo, IWICMetadataWriterInfo interface [Windows Imaging Component], IWICMetadataWriterInfo interface [Windows Imaging Component],described, _wic_codec_iwicmetadatawriterinfo, wic._wic_codec_iwicmetadatawriterinfo, wincodecsdk/IWICMetadataWriterInfo
ms.topic: interface
f1_keywords: 
 - "wincodecsdk/IWICMetadataWriterInfo"
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
 - IWICMetadataWriterInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataWriterInfo interface


## -description


Exposes methods that provide basic information about the registered metadata writer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataWriterInfo</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo">IWICMetadataHandlerInfo</a>. <b>IWICMetadataWriterInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataWriterInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatawriterinfo-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an instance of an <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatawriterinfo-getheader">GetHeader</a>
</td>
<td align="left" width="63%">
Gets the metadata header for the metadata writer.

</td>
</tr>
</table> 

