---
UID: NF:wmp.IWMPNetwork.get_bandWidth
title: IWMPNetwork::get_bandWidth (wmp.h)
description: The get_bandWidth method retrieves the current bandwidth of the media item.helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_bandWidth method","IWMPNetwork.get_bandWidth","IWMPNetwork::get_bandWidth","IWMPNetworkget_bandWidth","get_bandWidth","get_bandWidth method [Windows Media Player]","get_bandWidth method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_bandwidth","wmp/IWMPNetwork::get_bandWidth"]
old-location: wmp\iwmpnetwork_get_bandwidth.htm
tech.root: WMP
ms.assetid: 910356d8-3d43-4516-ad30-b0ed288e5098
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bandWidth method, IWMPNetwork.get_bandWidth, IWMPNetwork::get_bandWidth, IWMPNetworkget_bandWidth, get_bandWidth, get_bandWidth method [Windows Media Player], get_bandWidth method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bandwidth, wmp/IWMPNetwork::get_bandWidth
f1_keywords:
- wmp/IWMPNetwork.get_bandWidth
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPNetwork.get_bandWidth
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPNetwork::get_bandWidth


## -description



The <b>get_bandWidth</b> method retrieves the current bandwidth of the media item.




## -parameters




### -param plBandwidth [out]

Pointer to a <b>long</b> containing the bandwidth.


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



The value retrieved through <b>IWMPCore::put_URL</b> will be zero if the URL is not set. This method is only valid for streaming media.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>
 

 

