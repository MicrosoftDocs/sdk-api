---
UID: NF:wmp.IWMPClosedCaption.get_captioningId
title: IWMPClosedCaption::get_captioningId (wmp.h)
description: The get_captioningId method retrieves the name of the element displaying the captioning.
helpviewer_keywords: ["IWMPClosedCaption interface [Windows Media Player]","get_captioningId method","IWMPClosedCaption.get_captioningId","IWMPClosedCaption::get_captioningId","IWMPClosedCaptionget_captioningId","get_captioningId","get_captioningId method [Windows Media Player]","get_captioningId method [Windows Media Player]","IWMPClosedCaption interface","wmp.iwmpclosedcaption_get_captioningid","wmp/IWMPClosedCaption::get_captioningId"]
old-location: wmp\iwmpclosedcaption_get_captioningid.htm
tech.root: WMP
ms.assetid: c6aa1710-9686-439b-b098-7a3e5da532ee
ms.date: 4/26/2023
ms.keywords: IWMPClosedCaption interface [Windows Media Player],get_captioningId method, IWMPClosedCaption.get_captioningId, IWMPClosedCaption::get_captioningId, IWMPClosedCaptionget_captioningId, get_captioningId, get_captioningId method [Windows Media Player], get_captioningId method [Windows Media Player],IWMPClosedCaption interface, wmp.iwmpclosedcaption_get_captioningid, wmp/IWMPClosedCaption::get_captioningId
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
 - IWMPClosedCaption::get_captioningId
 - wmp/IWMPClosedCaption::get_captioningId
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
 - IWMPClosedCaption.get_captioningId
---

# IWMPClosedCaption::get_captioningId


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_captioningId</b> method retrieves the name of the element displaying the captioning.

## -parameters

### -param pbstrCaptioningID [out]

Pointer to a <b>BSTR</b> containing the captioning ID.

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

The element name specified can be any HTML element in the webpage as long as it supports the <b>innerHTML</b> attribute. If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Windows Media Player control.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.

## -see-also

<a href="/windows/desktop/WMP/adding-closed-captions-to-digital-media">Adding Closed Captions to Digital Media</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-put_captioningid">IWMPClosedCaption::put_captioningId</a>