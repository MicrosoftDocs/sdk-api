---
UID: NF:wmp.IWMPNetwork.getProxyBypassForLocal
title: IWMPNetwork::getProxyBypassForLocal (wmp.h)
description: The getProxyBypassForLocal method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","getProxyBypassForLocal method","IWMPNetwork.getProxyBypassForLocal","IWMPNetwork::getProxyBypassForLocal","IWMPNetworkgetProxyBypassForLocal","getProxyBypassForLocal","getProxyBypassForLocal method [Windows Media Player]","getProxyBypassForLocal method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_getproxybypassforlocal","wmp/IWMPNetwork::getProxyBypassForLocal"]
old-location: wmp\iwmpnetwork_getproxybypassforlocal.htm
tech.root: WMP
ms.assetid: 33cc24ab-9eb4-48ef-9483-058a3af04983
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],getProxyBypassForLocal method, IWMPNetwork.getProxyBypassForLocal, IWMPNetwork::getProxyBypassForLocal, IWMPNetworkgetProxyBypassForLocal, getProxyBypassForLocal, getProxyBypassForLocal method [Windows Media Player], getProxyBypassForLocal method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_getproxybypassforlocal, wmp/IWMPNetwork::getProxyBypassForLocal
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
 - IWMPNetwork::getProxyBypassForLocal
 - wmp/IWMPNetwork::getProxyBypassForLocal
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
 - IWMPNetwork.getProxyBypassForLocal
---

# IWMPNetwork::getProxyBypassForLocal


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getProxyBypassForLocal</b> method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.

## -parameters

### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol.

### -param pfBypassForLocal [out]

Pointer to a <b>VARIANT_BOOL</b> that indicates whether the proxy server is bypassed. The value retrieved is meaningful only when <b>IWMPNetwork::getProxySettings</b> retrieves a value of 2 (use manual settings).

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

This method fails unless the calling application is running on the local computer or intranet.

<b>Windows Media Player 10 Mobile:</b> This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxysettings">IWMPNetwork::getProxySettings</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxybypassforlocal">IWMPNetwork::setProxyBypassForLocal</a>