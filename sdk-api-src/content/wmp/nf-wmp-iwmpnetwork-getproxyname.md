---
UID: NF:wmp.IWMPNetwork.getProxyName
title: IWMPNetwork::getProxyName (wmp.h)
description: The getProxyName method retrieves the name of the proxy server being used.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","getProxyName method","IWMPNetwork.getProxyName","IWMPNetwork::getProxyName","IWMPNetworkgetProxyName","getProxyName","getProxyName method [Windows Media Player]","getProxyName method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_getproxyname","wmp/IWMPNetwork::getProxyName"]
old-location: wmp\iwmpnetwork_getproxyname.htm
tech.root: WMP
ms.assetid: 7bf3adaa-a89d-4ffe-8233-a9c606b39350
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],getProxyName method, IWMPNetwork.getProxyName, IWMPNetwork::getProxyName, IWMPNetworkgetProxyName, getProxyName, getProxyName method [Windows Media Player], getProxyName method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_getproxyname, wmp/IWMPNetwork::getProxyName
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
 - IWMPNetwork::getProxyName
 - wmp/IWMPNetwork::getProxyName
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
 - IWMPNetwork.getProxyName
---

# IWMPNetwork::getProxyName


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getProxyName</b> method retrieves the name of the proxy server being used.

## -parameters

### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="/windows/desktop/WMP/supported-protocols-and-file-types">Supported Protocols and File Types</a>.

### -param pbstrProxyName [out]

Pointer to a <b>BSTR</b> containing the name of the proxy server being used. The value retrieved is meaningful only when <b>IWMPNetwork::getProxySettings</b> retrieves a value of 2 (use manual settings).

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxyname">IWMPNetwork::setProxyName</a>