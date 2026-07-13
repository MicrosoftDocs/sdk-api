---
UID: NF:wmp.IWMPErrorItem.get_customUrl
title: IWMPErrorItem::get_customUrl (wmp.h)
description: The get_customUrl method retrieves the URL of a website that displays specific information about codec download failure.
helpviewer_keywords: ["IWMPErrorItem interface [Windows Media Player]","get_customUrl method","IWMPErrorItem.get_customUrl","IWMPErrorItem::get_customUrl","IWMPErrorItemget_customUrl","get_customUrl","get_customUrl method [Windows Media Player]","get_customUrl method [Windows Media Player]","IWMPErrorItem interface","wmp.iwmperroritem_get_customurl","wmp/IWMPErrorItem::get_customUrl"]
old-location: wmp\iwmperroritem_get_customurl.htm
tech.root: WMP
ms.assetid: 3cf54c10-a06d-49fc-aa8e-e6264ce23061
ms.date: 4/26/2023
ms.keywords: IWMPErrorItem interface [Windows Media Player],get_customUrl method, IWMPErrorItem.get_customUrl, IWMPErrorItem::get_customUrl, IWMPErrorItemget_customUrl, get_customUrl, get_customUrl method [Windows Media Player], get_customUrl method [Windows Media Player],IWMPErrorItem interface, wmp.iwmperroritem_get_customurl, wmp/IWMPErrorItem::get_customUrl
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
 - IWMPErrorItem::get_customUrl
 - wmp/IWMPErrorItem::get_customUrl
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
 - IWMPErrorItem.get_customUrl
---

# IWMPErrorItem::get_customUrl


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_customUrl</b> method retrieves the URL of a website that displays specific information about codec download failure.

## -parameters

### -param pbstrCustomUrl [out]

Pointer to a <b>BSTR</b> containing the custom url.

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

## -remarks

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmperroritem">IWMPErrorItem Interface</a>