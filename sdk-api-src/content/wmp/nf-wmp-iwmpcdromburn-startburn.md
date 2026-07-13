---
UID: NF:wmp.IWMPCdromBurn.startBurn
title: IWMPCdromBurn::startBurn (wmp.h)
description: The startBurn method burns the CD.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","startBurn method","IWMPCdromBurn.startBurn","IWMPCdromBurn::startBurn","IWMPCdromBurnstartBurn","startBurn","startBurn method [Windows Media Player]","startBurn method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_startburn","wmp/IWMPCdromBurn::startBurn"]
old-location: wmp\iwmpcdromburn_startburn.htm
tech.root: WMP
ms.assetid: 35357dca-4093-4c83-9cc9-f0dee1241e76
ms.date: 4/26/2023
ms.keywords: IWMPCdromBurn interface [Windows Media Player],startBurn method, IWMPCdromBurn.startBurn, IWMPCdromBurn::startBurn, IWMPCdromBurnstartBurn, startBurn, startBurn method [Windows Media Player], startBurn method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_startburn, wmp/IWMPCdromBurn::startBurn
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
 - IWMPCdromBurn::startBurn
 - wmp/IWMPCdromBurn::startBurn
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
 - IWMPCdromBurn.startBurn
---

# IWMPCdromBurn::startBurn


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>startBurn</b> method burns the CD.



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

The burn state should be wmpbsReady or wmpbsStopped before calling this method.

This method will not work if the CD drive is not a burner, or if the disc in the drive is not writable. Use <a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable">IWMPCdromBurn::isAvailable</a> to determine whether a CD can be burned.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate">IWMPCdromBurn::get_burnState</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn">IWMPCdromBurn::stopBurn</a>
