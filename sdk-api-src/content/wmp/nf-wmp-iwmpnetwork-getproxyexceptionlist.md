---
UID: NF:wmp.IWMPNetwork.getProxyExceptionList
title: IWMPNetwork::getProxyExceptionList (wmp.h)
description: The getProxyExceptionList method retrieves the proxy exception list.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","getProxyExceptionList method","IWMPNetwork.getProxyExceptionList","IWMPNetwork::getProxyExceptionList","IWMPNetworkgetProxyExceptionList","getProxyExceptionList","getProxyExceptionList method [Windows Media Player]","getProxyExceptionList method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_getproxyexceptionlist","wmp/IWMPNetwork::getProxyExceptionList"]
old-location: wmp\iwmpnetwork_getproxyexceptionlist.htm
tech.root: WMP
ms.assetid: ddd3a6b2-3637-4da1-b3ce-f01364e8b818
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],getProxyExceptionList method, IWMPNetwork.getProxyExceptionList, IWMPNetwork::getProxyExceptionList, IWMPNetworkgetProxyExceptionList, getProxyExceptionList, getProxyExceptionList method [Windows Media Player], getProxyExceptionList method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_getproxyexceptionlist, wmp/IWMPNetwork::getProxyExceptionList
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
 - IWMPNetwork::getProxyExceptionList
 - wmp/IWMPNetwork::getProxyExceptionList
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
 - IWMPNetwork.getProxyExceptionList
---

# IWMPNetwork::getProxyExceptionList


## -description

The <b>getProxyExceptionList</b> method retrieves the proxy exception list.

## -parameters

### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="/windows/desktop/WMP/supported-protocols-and-file-types">Supported Protocols and File Types</a>.

### -param pbstrExceptionList [out]

Pointer to a <b>BSTR</b> containing a semicolon-delimited list of hosts for which the proxy server is bypassed. The value retrieved is meaningful only when <b>IWMPNetwork::getProxySettings</b> retrieves a value of 2 (use manual settings).

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

This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.

The * character can be used as a wildcard for listing entries. For example, *.com would match all hosts in the com domain while 67.* would match all hosts in the 67 class A subnet.

This method fails unless the calling application is running on the local computer or intranet.

<b>Windows Media Player 10 Mobile:</b> This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxysettings">IWMPNetwork::getProxySettings</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxyexceptionlist">IWMPNetwork::setProxyExceptionList</a>