---
UID: NF:wmp.IWMPMetadataText.get_text
title: IWMPMetadataText::get_text (wmp.h)
description: The get_text method retrieves the metadata text.
helpviewer_keywords: ["IWMPMetadataText interface [Windows Media Player]","get_text method","IWMPMetadataText.get_text","IWMPMetadataText::get_text","IWMPMetadataTextget_text","get_text","get_text method [Windows Media Player]","get_text method [Windows Media Player]","IWMPMetadataText interface","wmp.iwmpmetadatatext_get_text","wmp/IWMPMetadataText::get_text"]
old-location: wmp\iwmpmetadatatext_get_text.htm
tech.root: WMP
ms.assetid: 88aeb4bb-87e1-413d-888b-608fa349ebf5
ms.date: 4/26/2023
ms.keywords: IWMPMetadataText interface [Windows Media Player],get_text method, IWMPMetadataText.get_text, IWMPMetadataText::get_text, IWMPMetadataTextget_text, get_text, get_text method [Windows Media Player], get_text method [Windows Media Player],IWMPMetadataText interface, wmp.iwmpmetadatatext_get_text, wmp/IWMPMetadataText::get_text
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
 - IWMPMetadataText::get_text
 - wmp/IWMPMetadataText::get_text
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
 - IWMPMetadataText.get_text
---

# IWMPMetadataText::get_text


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_text</b> method retrieves the metadata text.

## -parameters

### -param pbstrText [out]

Pointer to a <b>BSTR</b> containing the text.

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

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext">IWMPMetadataText Interface</a>