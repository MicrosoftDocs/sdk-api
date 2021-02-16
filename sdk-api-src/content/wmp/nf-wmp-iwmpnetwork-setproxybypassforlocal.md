---
UID: NF:wmp.IWMPNetwork.setProxyBypassForLocal
title: IWMPNetwork::setProxyBypassForLocal (wmp.h)
description: The setProxyBypassForLocal method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","setProxyBypassForLocal method","IWMPNetwork.setProxyBypassForLocal","IWMPNetwork::setProxyBypassForLocal","IWMPNetworksetProxyBypassForLocal","setProxyBypassForLocal","setProxyBypassForLocal method [Windows Media Player]","setProxyBypassForLocal method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_setproxybypassforlocal","wmp/IWMPNetwork::setProxyBypassForLocal"]
old-location: wmp\iwmpnetwork_setproxybypassforlocal.htm
tech.root: WMP
ms.assetid: 4477bc81-e52b-4924-a31b-6f005a5bd158
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],setProxyBypassForLocal method, IWMPNetwork.setProxyBypassForLocal, IWMPNetwork::setProxyBypassForLocal, IWMPNetworksetProxyBypassForLocal, setProxyBypassForLocal, setProxyBypassForLocal method [Windows Media Player], setProxyBypassForLocal method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_setproxybypassforlocal, wmp/IWMPNetwork::setProxyBypassForLocal
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
 - IWMPNetwork::setProxyBypassForLocal
 - wmp/IWMPNetwork::setProxyBypassForLocal
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
 - IWMPNetwork.setProxyBypassForLocal
---

# IWMPNetwork::setProxyBypassForLocal


## -description

The <b>setProxyBypassForLocal</b> method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.

## -parameters

### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="/windows/desktop/WMP/supported-protocols-and-file-types">Supported Protocols and File Types</a>.

### -param fBypassForLocal [in]

<b>VARIANT_BOOL</b> indicating whether the proxy server is bypassed.

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

This method has no effect unless the value retrieved from <b>IWMPNetwork::getProxySettings</b> is 2 (use manual settings).

This method fails unless the calling application is running on the local computer or intranet.

<b>Windows Media Player 10 Mobile:</b> This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxybypassforlocal">IWMPNetwork::getProxyBypassForLocal</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxysettings">IWMPNetwork::getProxySettings</a>