---
UID: NF:wmp.IWMPCdromBurn.refreshStatus
title: IWMPCdromBurn::refreshStatus (wmp.h)
description: The refreshStatus method updates the status information for the current burn playlist.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","refreshStatus method","IWMPCdromBurn.refreshStatus","IWMPCdromBurn::refreshStatus","IWMPCdromBurnrefreshStatus","refreshStatus","refreshStatus method [Windows Media Player]","refreshStatus method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_refreshstatus","wmp/IWMPCdromBurn::refreshStatus"]
old-location: wmp\iwmpcdromburn_refreshstatus.htm
tech.root: WMP
ms.assetid: 7a1ca071-0a61-4ef5-b8c1-18336cf5b1b0
ms.date: 12/05/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],refreshStatus method, IWMPCdromBurn.refreshStatus, IWMPCdromBurn::refreshStatus, IWMPCdromBurnrefreshStatus, refreshStatus, refreshStatus method [Windows Media Player], refreshStatus method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_refreshstatus, wmp/IWMPCdromBurn::refreshStatus
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
 - IWMPCdromBurn::refreshStatus
 - wmp/IWMPCdromBurn::refreshStatus
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
 - IWMPCdromBurn.refreshStatus
---

# IWMPCdromBurn::refreshStatus


## -description

The <b>refreshStatus</b> method updates the status information for the current burn playlist.



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

You should call this method after you create or change a burn playlist before reading status information or burning the CD. You can test whether a refresh is required by calling <b>get_burnState</b> and checking for wmpbsRefreshStatusPending.

Refreshing the status is a synchronous operation. This means that a lengthy period of time might elapse before this method returns if the current burn playlist is large and contains many changes.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate">IWMPCdromBurn::get_burnState</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpburnstate">WMPBurnState</a>
