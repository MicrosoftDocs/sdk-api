---
UID: NF:wmp.IWMPCdromRip.startRip
title: IWMPCdromRip::startRip (wmp.h)
description: The startRip method rips the CD.
helpviewer_keywords: ["IWMPCdromRip interface [Windows Media Player]","startRip method","IWMPCdromRip.startRip","IWMPCdromRip::startRip","IWMPCdromRipstartRip","startRip","startRip method [Windows Media Player]","startRip method [Windows Media Player]","IWMPCdromRip interface","wmp.iwmpcdromrip_startrip","wmp/IWMPCdromRip::startRip"]
old-location: wmp\iwmpcdromrip_startrip.htm
tech.root: WMP
ms.assetid: 88ba1e83-a3c5-4922-8c58-37993ccb4afc
ms.date: 4/26/2023
ms.keywords: IWMPCdromRip interface [Windows Media Player],startRip method, IWMPCdromRip.startRip, IWMPCdromRip::startRip, IWMPCdromRipstartRip, startRip, startRip method [Windows Media Player], startRip method [Windows Media Player],IWMPCdromRip interface, wmp.iwmpcdromrip_startrip, wmp/IWMPCdromRip::startRip
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
 - IWMPCdromRip::startRip
 - wmp/IWMPCdromRip::startRip
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
 - IWMPCdromRip.startRip
---

# IWMPCdromRip::startRip


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>startRip</b> method rips the CD.



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

Ripping a CD by using the <b>IWMPCdromRip</b> interface has the same effect as ripping music by using the Windows Media Player user interface. Ripped content is automatically added to the library according to the user's preferences. For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip">IWMPCdromRip Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip">IWMPCdromRip::stopRip</a>



<a href="/windows/desktop/WMP/ripping-a-cd">Ripping a CD</a>
