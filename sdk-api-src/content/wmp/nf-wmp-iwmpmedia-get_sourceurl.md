---
UID: NF:wmp.IWMPMedia.get_sourceURL
title: IWMPMedia::get_sourceURL (wmp.h)
description: The get_sourceURL method retrieves the URL of the media item.
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","get_sourceURL method","IWMPMedia.get_sourceURL","IWMPMedia2 interface [Windows Media Player]","get_sourceURL method","IWMPMedia2::get_sourceURL","IWMPMedia3 interface [Windows Media Player]","get_sourceURL method","IWMPMedia3::get_sourceURL","IWMPMedia::get_sourceURL","IWMPMediaget_sourceURL","get_sourceURL","get_sourceURL method [Windows Media Player]","get_sourceURL method [Windows Media Player]","IWMPMedia interface","get_sourceURL method [Windows Media Player]","IWMPMedia2 interface","get_sourceURL method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_get_sourceurl","wmp/IWMPMedia2::get_sourceURL","wmp/IWMPMedia3::get_sourceURL","wmp/IWMPMedia::get_sourceURL"]
old-location: wmp\iwmpmedia_get_sourceurl.htm
tech.root: WMP
ms.assetid: 99a9bd0f-0429-41b0-96fc-b84d895f6b38
ms.date: 12/05/2018
ms.keywords: IWMPMedia interface [Windows Media Player],get_sourceURL method, IWMPMedia.get_sourceURL, IWMPMedia2 interface [Windows Media Player],get_sourceURL method, IWMPMedia2::get_sourceURL, IWMPMedia3 interface [Windows Media Player],get_sourceURL method, IWMPMedia3::get_sourceURL, IWMPMedia::get_sourceURL, IWMPMediaget_sourceURL, get_sourceURL, get_sourceURL method [Windows Media Player], get_sourceURL method [Windows Media Player],IWMPMedia interface, get_sourceURL method [Windows Media Player],IWMPMedia2 interface, get_sourceURL method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_sourceurl, wmp/IWMPMedia2::get_sourceURL, wmp/IWMPMedia3::get_sourceURL, wmp/IWMPMedia::get_sourceURL
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPMedia::get_sourceURL
 - wmp/IWMPMedia::get_sourceURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPMedia.get_sourceURL
 - IWMPMedia2.get_sourceURL
 - IWMPMedia3.get_sourceURL
---

# IWMPMedia::get_sourceURL


## -description

The <b>get_sourceURL</b> method retrieves the URL of the media item.

## -parameters

### -param pbstrSourceURL [out]

Pointer to a <b>BSTR</b> containing the source URL.

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
</table>

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>