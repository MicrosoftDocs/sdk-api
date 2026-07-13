---
UID: NF:wmp.IWMPNetwork.setProxyExceptionList
title: IWMPNetwork::setProxyExceptionList (wmp.h)
description: The setProxyExceptionList method specifies the proxy exception list.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","setProxyExceptionList method","IWMPNetwork.setProxyExceptionList","IWMPNetwork::setProxyExceptionList","IWMPNetworksetProxyExceptionList","setProxyExceptionList","setProxyExceptionList method [Windows Media Player]","setProxyExceptionList method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_setproxyexceptionlist","wmp/IWMPNetwork::setProxyExceptionList"]
old-location: wmp\iwmpnetwork_setproxyexceptionlist.htm
tech.root: WMP
ms.assetid: af9202aa-fa4e-4726-908f-3fc5370e06df
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],setProxyExceptionList method, IWMPNetwork.setProxyExceptionList, IWMPNetwork::setProxyExceptionList, IWMPNetworksetProxyExceptionList, setProxyExceptionList, setProxyExceptionList method [Windows Media Player], setProxyExceptionList method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_setproxyexceptionlist, wmp/IWMPNetwork::setProxyExceptionList
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
 - IWMPNetwork::setProxyExceptionList
 - wmp/IWMPNetwork::setProxyExceptionList
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
 - IWMPNetwork.setProxyExceptionList
---

# IWMPNetwork::setProxyExceptionList


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>setProxyExceptionList</b> method specifies the proxy exception list.

## -parameters

### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="/windows/desktop/WMP/supported-protocols-and-file-types">Supported Protocols and File Types</a>.

### -param pbstrExceptionList [in]

<b>BSTR</b> containing a semicolon-delimited list of hosts for which the proxy server is bypassed. Leading and trailing spaces should not be present.

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

The * character can be used as a wildcard for listing entries. For example, *.com would match all hosts in the com domain, while 67.* would match all hosts in the 67 class A subnet.

This method has no effect unless the value retrieved from <b>IWMPNetwork::getProxySettings</b> is 2 (use manual settings).

This method fails unless the calling application is running on the local computer or intranet.

<b>Windows Media Player 10 Mobile:</b> This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxyexceptionlist">IWMPNetwork::getProxyExceptionList</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxysettings">IWMPNetwork::getProxySettings</a>