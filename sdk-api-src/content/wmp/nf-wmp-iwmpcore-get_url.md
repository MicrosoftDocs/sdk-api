---
UID: NF:wmp.IWMPCore.get_URL
title: IWMPCore::get_URL (wmp.h)
description: The get_URL method retrieves the name of the clip to play.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_URL method","IWMPCore.get_URL","IWMPCore::get_URL","IWMPCoreget_URL","get_URL","get_URL method [Windows Media Player]","get_URL method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_url","wmp/IWMPCore::get_URL"]
old-location: wmp\iwmpcore_get_url.htm
tech.root: WMP
ms.assetid: 54d43a1c-807a-40a5-a703-262d75f88ca0
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],get_URL method, IWMPCore.get_URL, IWMPCore::get_URL, IWMPCoreget_URL, get_URL, get_URL method [Windows Media Player], get_URL method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_url, wmp/IWMPCore::get_URL
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
 - IWMPCore::get_URL
 - wmp/IWMPCore::get_URL
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
 - IWMPCore.get_URL
---

# IWMPCore::get_URL


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_URL</b> method retrieves the name of the clip to play.

## -parameters

### -param pbstrURL [out]

Pointer to a <b>BSTR</b> containing the URL.

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

Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.

Calling this method from an event handler may yield unexpected results.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>