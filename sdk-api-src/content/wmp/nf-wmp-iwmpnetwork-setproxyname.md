---
UID: NF:wmp.IWMPNetwork.setProxyName
title: IWMPNetwork::setProxyName (wmp.h)
description: The setProxyName method specifies the name of the proxy server to use.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","setProxyName method","IWMPNetwork.setProxyName","IWMPNetwork::setProxyName","IWMPNetworksetProxyName","setProxyName","setProxyName method [Windows Media Player]","setProxyName method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_setproxyname","wmp/IWMPNetwork::setProxyName"]
old-location: wmp\iwmpnetwork_setproxyname.htm
tech.root: WMP
ms.assetid: 6f484f5b-195c-496d-932e-3e1fdbf873d8
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],setProxyName method, IWMPNetwork.setProxyName, IWMPNetwork::setProxyName, IWMPNetworksetProxyName, setProxyName, setProxyName method [Windows Media Player], setProxyName method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_setproxyname, wmp/IWMPNetwork::setProxyName
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
 - IWMPNetwork::setProxyName
 - wmp/IWMPNetwork::setProxyName
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
 - IWMPNetwork.setProxyName
---

# IWMPNetwork::setProxyName


## -description

The <b>setProxyName</b> method specifies the name of the proxy server to use.

## -parameters

### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="/windows/desktop/WMP/supported-protocols-and-file-types">Supported Protocols and File Types</a>.

### -param bstrProxyName [in]

<b>BSTR</b> containing the name of the proxy server to use.

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxyname">IWMPNetwork::getProxyName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxysettings">IWMPNetwork::getProxySettings</a>