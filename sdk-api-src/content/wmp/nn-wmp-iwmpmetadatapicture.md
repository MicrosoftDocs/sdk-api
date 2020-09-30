---
UID: NN:wmp.IWMPMetadataPicture
title: IWMPMetadataPicture (wmp.h)
description: The IWMPMetadataPicture interface provides methods for retrieving information about the WM/Picture metadata attribute.
helpviewer_keywords: ["IWMPMetadataPicture","IWMPMetadataPicture interface [Windows Media Player]","IWMPMetadataPicture interface [Windows Media Player]","described","IWMPMetadataPictureInterface","wmp.iwmpmetadatapicture","wmp/IWMPMetadataPicture"]
old-location: wmp\iwmpmetadatapicture.htm
tech.root: WMP
ms.assetid: 385819d0-cf27-4f39-86be-140d1bc87d12
ms.date: 12/05/2018
ms.keywords: IWMPMetadataPicture, IWMPMetadataPicture interface [Windows Media Player], IWMPMetadataPicture interface [Windows Media Player],described, IWMPMetadataPictureInterface, wmp.iwmpmetadatapicture, wmp/IWMPMetadataPicture
req.header: wmp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPMetadataPicture
 - wmp/IWMPMetadataPicture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPMetadataPicture
---

# IWMPMetadataPicture interface


## -description

The <b>IWMPMetadataPicture</b> interface provides methods for retrieving information about the <a href="/windows/desktop/wmformat/wmpicture">WM/Picture</a> metadata attribute.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPMetadataPicture</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPMetadataPicture</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPMetadataPicture</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmetadatapicture-get_description">get_description</a>
</td>
<td align="left" width="63%">
Retrieves a description of the metadata image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmetadatapicture-get_mimetype">get_mimeType</a>
</td>
<td align="left" width="63%">
Retrieves the MIME type of the metadata image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmetadatapicture-get_picturetype">get_pictureType</a>
</td>
<td align="left" width="63%">
Retrieves the picture type of the metadata image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmetadatapicture-get_url">get_URL</a>
</td>
<td align="left" width="63%">
Internal use only.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/WMP/interfaces">Interfaces</a>