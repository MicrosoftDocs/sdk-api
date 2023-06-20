---
UID: NF:wmp.IWMPCore.close
title: IWMPCore::close (wmp.h)
description: The close method releases Windows Media Player resources.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","close method","IWMPCore.close","IWMPCore::close","IWMPCoreclose","close","close method [Windows Media Player]","close method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_close","wmp/IWMPCore::close"]
old-location: wmp\iwmpcore_close.htm
tech.root: WMP
ms.assetid: e6e21995-5dbd-4893-a9f2-6ce918d3fbc4
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],close method, IWMPCore.close, IWMPCore::close, IWMPCoreclose, close, close method [Windows Media Player], close method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_close, wmp/IWMPCore::close
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
 - IWMPCore::close
 - wmp/IWMPCore::close
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
 - IWMPCore.close
---

# IWMPCore::close


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>close</b> method releases Windows Media Player resources.



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

This method closes the current digital media file, not Windows Media Player.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>
