---
UID: NF:wmp.IWMPNetwork.setProxyBypassForLocal
title: IWMPNetwork::setProxyBypassForLocal
author: windows-sdk-content
description: The setProxyBypassForLocal method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.
old-location: wmp\iwmpnetwork_setproxybypassforlocal.htm
tech.root: WMP
ms.assetid: 4477bc81-e52b-4924-a31b-6f005a5bd158
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],setProxyBypassForLocal method, IWMPNetwork.setProxyBypassForLocal, IWMPNetwork::setProxyBypassForLocal, IWMPNetworksetProxyBypassForLocal, setProxyBypassForLocal, setProxyBypassForLocal method [Windows Media Player], setProxyBypassForLocal method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_setproxybypassforlocal, wmp/IWMPNetwork::setProxyBypassForLocal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWMPNetwork.setProxyBypassForLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPNetwork.setProxyBypassForLocal
: 
---

# IWMPNetwork::setProxyBypassForLocal


## -description



The <b>setProxyBypassForLocal</b> method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.




## -parameters




### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="https://msdn.microsoft.com/2672372c-0b42-437e-8b96-83b6e5200fd3">Supported Protocols and File Types</a>.


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




<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/33cc24ab-9eb4-48ef-9483-058a3af04983">IWMPNetwork::getProxyBypassForLocal</a>



<a href="https://msdn.microsoft.com/103e0d53-943d-4aba-9db1-20cdc1d75d52">IWMPNetwork::getProxySettings</a>
 

 

