---
UID: NF:wmp.IWMPCdromRip.stopRip
title: IWMPCdromRip::stopRip (wmp.h)
description: The stopRip method stops the CD ripping process.
helpviewer_keywords: ["IWMPCdromRip interface [Windows Media Player]","stopRip method","IWMPCdromRip.stopRip","IWMPCdromRip::stopRip","IWMPCdromRipstopRip","stopRip","stopRip method [Windows Media Player]","stopRip method [Windows Media Player]","IWMPCdromRip interface","wmp.iwmpcdromrip_stoprip","wmp/IWMPCdromRip::stopRip"]
old-location: wmp\iwmpcdromrip_stoprip.htm
tech.root: WMP
ms.assetid: 2a6c5a25-f69c-4258-a92f-7f693b201a01
ms.date: 12/05/2018
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

The <b>stopRip</b> method stops the CD ripping process.

## -parameters

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