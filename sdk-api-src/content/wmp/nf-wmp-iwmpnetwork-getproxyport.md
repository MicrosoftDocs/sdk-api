---
UID: NF:wmp.IWMPNetwork.getProxyPort
title: IWMPNetwork::getProxyPort (wmp.h)
description: The getProxyPort method retrieves the proxy port being used.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","getProxyPort method","IWMPNetwork.getProxyPort","IWMPNetwork::getProxyPort","IWMPNetworkgetProxyPort","getProxyPort","getProxyPort method [Windows Media Player]","getProxyPort method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_getproxyport","wmp/IWMPNetwork::getProxyPort"]
old-location: wmp\iwmpnetwork_getproxyport.htm
tech.root: WMP
ms.assetid: 0d636e61-a5c1-495a-8d1d-ce2937dd3f18
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],getProxyPort method, IWMPNetwork.getProxyPort, IWMPNetwork::getProxyPort, IWMPNetworkgetProxyPort, getProxyPort, getProxyPort method [Windows Media Player], getProxyPort method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_getproxyport, wmp/IWMPNetwork::getProxyPort
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
 - IWMPNetwork::getProxyPort
 - wmp/IWMPNetwork::getProxyPort
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
 - IWMPNetwork.getProxyPort
---

# IWMPNetwork::getProxyPort


## -description

The <b>getProxyPort</b> method retrieves the proxy port being used.

## -parameters

### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="/windows/desktop/WMP/supported-protocols-and-file-types">Supported Protocols and File Types</a>.

### -param lProxyPort [out]

<b>long</b> containing the proxy port being used. The value retrieved is meaningful only when <b>IWMPNetwork::getProxySettings</b> retrieves a value of 2 (use manual settings).

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxyport">IWMPNetwork::setProxyPort</a>