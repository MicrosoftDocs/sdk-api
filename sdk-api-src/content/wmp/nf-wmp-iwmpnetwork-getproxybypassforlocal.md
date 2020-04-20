---
UID: NF:wmp.IWMPNetwork.getProxyBypassForLocal
title: IWMPNetwork::getProxyBypassForLocal (wmp.h)
description: The getProxyBypassForLocal method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","getProxyBypassForLocal method","IWMPNetwork.getProxyBypassForLocal","IWMPNetwork::getProxyBypassForLocal","IWMPNetworkgetProxyBypassForLocal","getProxyBypassForLocal","getProxyBypassForLocal method [Windows Media Player]","getProxyBypassForLocal method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_getproxybypassforlocal","wmp/IWMPNetwork::getProxyBypassForLocal"]
old-location: wmp\iwmpnetwork_getproxybypassforlocal.htm
tech.root: WMP
ms.assetid: 33cc24ab-9eb4-48ef-9483-058a3af04983
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],getProxyBypassForLocal method, IWMPNetwork.getProxyBypassForLocal, IWMPNetwork::getProxyBypassForLocal, IWMPNetworkgetProxyBypassForLocal, getProxyBypassForLocal, getProxyBypassForLocal method [Windows Media Player], getProxyBypassForLocal method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_getproxybypassforlocal, wmp/IWMPNetwork::getProxyBypassForLocal
f1_keywords:
- wmp/IWMPNetwork.getProxyBypassForLocal
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
- IWMPNetwork.getProxyBypassForLocal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPNetwork::getProxyBypassForLocal


## -description



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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxysettings">IWMPNetwork::getProxySettings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxybypassforlocal">IWMPNetwork::setProxyBypassForLocal</a>
 

 

