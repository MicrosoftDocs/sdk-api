---
UID: NN:wmcodecdsp.IWMCodecPrivateData
title: IWMCodecPrivateData (wmcodecdsp.h)
description: Gets the private codec data that must be appended to the output media type. This codec data is required for properly decoding Windows Media Video content.
helpviewer_keywords: ["IWMCodecPrivateData","IWMCodecPrivateData interface [Media Foundation]","IWMCodecPrivateData interface [Media Foundation]","described","codecapi.iwmcodecprivatedata","codecapi.iwmcodecprivatedatainterface","mf.iwmcodecprivatedatainterface","wmcodecdsp/IWMCodecPrivateData"]
old-location: mf\iwmcodecprivatedatainterface.htm
tech.root: medfound
ms.assetid: c1216fd7-7cbd-45cf-b694-a5fd9a972fcd
ms.date: 12/05/2018
ms.keywords: IWMCodecPrivateData, IWMCodecPrivateData interface [Media Foundation], IWMCodecPrivateData interface [Media Foundation],described, codecapi.iwmcodecprivatedata, codecapi.iwmcodecprivatedatainterface, mf.iwmcodecprivatedatainterface, wmcodecdsp/IWMCodecPrivateData
f1_keywords:
- wmcodecdsp/IWMCodecPrivateData
dev_langs:
- c++
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmcodecdsp.h
api_name:
- IWMCodecPrivateData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMCodecPrivateData interface


## -description


Gets the private codec data that must be appended to the output media type. This codec data is required for properly decoding Windows Media Video content.

This interface is implemented by the video encoder object and the screen capture encoder object. You do not need codec private data to decode content of the subtype WMCMEDIASUBTYPE_WMV1 (Windows Media Video version 7). For any other output type, you must obtain a pointer to the encoder's IWMCodecPrivateData interface by calling the QueryInterface method of any other interface on the object, such as IMediaObject or IMFTransform.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecPrivateData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecPrivateData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecPrivateData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata">GetPrivateData</a>
</td>
<td align="left" width="63%">
Retrieves the codec data for the output type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype">SetPartialOutputType</a>
</td>
<td align="left" width="63%">
Gives the codec the output media type without the codec data. The codec needs this information to generate the private data.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

