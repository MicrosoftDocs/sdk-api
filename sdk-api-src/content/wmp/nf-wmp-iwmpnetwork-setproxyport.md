---
UID: NF:wmp.IWMPNetwork.setProxyPort
title: IWMPNetwork::setProxyPort (wmp.h)
description: The setProxyPort method specifies the proxy port to use.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","setProxyPort method","IWMPNetwork.setProxyPort","IWMPNetwork::setProxyPort","IWMPNetworksetProxyPort","setProxyPort","setProxyPort method [Windows Media Player]","setProxyPort method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_setproxyport","wmp/IWMPNetwork::setProxyPort"]
old-location: wmp\iwmpnetwork_setproxyport.htm
tech.root: WMP
ms.assetid: 36b7290d-c359-45bb-b77b-46b696e9edcf
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],setProxyPort method, IWMPNetwork.setProxyPort, IWMPNetwork::setProxyPort, IWMPNetworksetProxyPort, setProxyPort, setProxyPort method [Windows Media Player], setProxyPort method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_setproxyport, wmp/IWMPNetwork::setProxyPort
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
 - IWMPNetwork::setProxyPort
 - wmp/IWMPNetwork::setProxyPort
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
 - IWMPNetwork.setProxyPort
---

# IWMPNetwork::setProxyPort


## -description

The <b>setProxyPort</b> method specifies the proxy port to use.

## -parameters

### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="/windows/desktop/WMP/supported-protocols-and-file-types">Supported Protocols and File Types</a>..

### -param lProxyPort [in]

<b>long</b> containing the proxy port to use.

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxyport">IWMPNetwork::getProxyPort</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxysettings">IWMPNetwork::getProxySettings</a>