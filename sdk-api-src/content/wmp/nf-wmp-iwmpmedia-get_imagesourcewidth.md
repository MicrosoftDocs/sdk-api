---
UID: NF:wmp.IWMPMedia.get_imageSourceWidth
title: IWMPMedia::get_imageSourceWidth (wmp.h)
description: The get_imageSourceWidth method retrieves the width of the current media item in pixels.
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","get_imageSourceWidth method","IWMPMedia.get_imageSourceWidth","IWMPMedia2 interface [Windows Media Player]","get_imageSourceWidth method","IWMPMedia2::get_imageSourceWidth","IWMPMedia3 interface [Windows Media Player]","get_imageSourceWidth method","IWMPMedia3::get_imageSourceWidth","IWMPMedia::get_imageSourceWidth","IWMPMediaget_imageSourceWidth","get_imageSourceWidth","get_imageSourceWidth method [Windows Media Player]","get_imageSourceWidth method [Windows Media Player]","IWMPMedia interface","get_imageSourceWidth method [Windows Media Player]","IWMPMedia2 interface","get_imageSourceWidth method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_get_imagesourcewidth","wmp/IWMPMedia2::get_imageSourceWidth","wmp/IWMPMedia3::get_imageSourceWidth","wmp/IWMPMedia::get_imageSourceWidth"]
old-location: wmp\iwmpmedia_get_imagesourcewidth.htm
tech.root: WMP
ms.assetid: 57480abb-9852-46a5-a6e4-2a1ba517a9cb
ms.date: 4/26/2023
ms.keywords: IWMPMedia interface [Windows Media Player],get_imageSourceWidth method, IWMPMedia.get_imageSourceWidth, IWMPMedia2 interface [Windows Media Player],get_imageSourceWidth method, IWMPMedia2::get_imageSourceWidth, IWMPMedia3 interface [Windows Media Player],get_imageSourceWidth method, IWMPMedia3::get_imageSourceWidth, IWMPMedia::get_imageSourceWidth, IWMPMediaget_imageSourceWidth, get_imageSourceWidth, get_imageSourceWidth method [Windows Media Player], get_imageSourceWidth method [Windows Media Player],IWMPMedia interface, get_imageSourceWidth method [Windows Media Player],IWMPMedia2 interface, get_imageSourceWidth method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_imagesourcewidth, wmp/IWMPMedia2::get_imageSourceWidth, wmp/IWMPMedia3::get_imageSourceWidth, wmp/IWMPMedia::get_imageSourceWidth
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
 - IWMPMedia::get_imageSourceWidth
 - wmp/IWMPMedia::get_imageSourceWidth
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
 - IWMPMedia.get_imageSourceWidth
 - IWMPMedia2.get_imageSourceWidth
 - IWMPMedia3.get_imageSourceWidth
---

# IWMPMedia::get_imageSourceWidth


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_imageSourceWidth</b> method retrieves the width of the current media item in pixels.

## -parameters

### -param pWidth [out]

Pointer to a <b>long</b> that specifies the width.

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

If the digital media item is not the current one, this property returns zero.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>