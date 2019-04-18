---
UID: NN:wincodecsdk.IWICMetadataReaderInfo
title: IWICMetadataReaderInfo (wincodecsdk.h)
author: windows-sdk-content
description: Exposes methods that provide basic information about the registered metadata reader.
old-location: wic\_wic_codec_iwicmetadatareaderinfo.htm
tech.root: wic
ms.assetid: f72d9a06-0568-4e46-a904-202aad2f8859
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICMetadataReaderInfo, IWICMetadataReaderInfo interface [Windows Imaging Component], IWICMetadataReaderInfo interface [Windows Imaging Component],described, _wic_codec_iwicmetadatareaderinfo, wic._wic_codec_iwicmetadatareaderinfo, wincodecsdk/IWICMetadataReaderInfo
ms.topic: interface
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
 - IWICMetadataReaderInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataReaderInfo interface


## -description


Exposes methods that provide basic information about the registered metadata reader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataReaderInfo</b> interface inherits from <a href="https://msdn.microsoft.com/505105c2-de50-4b5f-9089-e9a3cea2f464">IWICMetadataHandlerInfo</a>. <b>IWICMetadataReaderInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataReaderInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6ee4ee9-8d9d-44f7-aab8-8e8ccfa7f942">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an instance of an <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc0033f7-801d-4ae0-a2cb-bdda25303476">GetPatterns</a>
</td>
<td align="left" width="63%">
Gets the metadata patterns associated with the metadata reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58ac58f4-25e0-4fc4-8d2a-854bb89e4af6">MatchesPattern</a>
</td>
<td align="left" width="63%">
Determines if a stream contains a metadata item pattern.

</td>
</tr>
</table> 

