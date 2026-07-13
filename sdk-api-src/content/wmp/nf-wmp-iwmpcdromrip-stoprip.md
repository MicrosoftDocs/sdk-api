---
UID: NF:wmp.IWMPCdromRip.stopRip
title: IWMPCdromRip::stopRip (wmp.h)
description: The stopRip method stops the CD ripping process.
helpviewer_keywords: ["IWMPCdromRip interface [Windows Media Player]","stopRip method","IWMPCdromRip.stopRip","IWMPCdromRip::stopRip","IWMPCdromRipstopRip","stopRip","stopRip method [Windows Media Player]","stopRip method [Windows Media Player]","IWMPCdromRip interface","wmp.iwmpcdromrip_stoprip","wmp/IWMPCdromRip::stopRip"]
old-location: wmp\iwmpcdromrip_stoprip.htm
tech.root: WMP
ms.assetid: 2a6c5a25-f69c-4258-a92f-7f693b201a01
ms.date: 4/26/2023
ms.keywords: IWMPCdromRip interface [Windows Media Player],stopRip method, IWMPCdromRip.stopRip, IWMPCdromRip::stopRip, IWMPCdromRipstopRip, stopRip, stopRip method [Windows Media Player], stopRip method [Windows Media Player],IWMPCdromRip interface, wmp.iwmpcdromrip_stoprip, wmp/IWMPCdromRip::stopRip
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPCdromRip::stopRip
 - wmp/IWMPCdromRip::stopRip
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
 - IWMPCdromRip.stopRip
---

# IWMPCdromRip::stopRip


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>stopRip</b> method stops the CD ripping process.



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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip">IWMPCdromRip Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip">IWMPCdromRip::startRip</a>



<a href="/windows/desktop/WMP/ripping-a-cd">Ripping a CD</a>
