---
UID: NF:wmp.IWMPNetwork.getProxyName
title: IWMPNetwork::getProxyName
author: windows-sdk-content
description: The getProxyName method retrieves the name of the proxy server being used.
old-location: wmp\iwmpnetwork_getproxyname.htm
old-project: WMP
ms.assetid: 7bf3adaa-a89d-4ffe-8233-a9c606b39350
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],getProxyName method, IWMPNetwork.getProxyName, IWMPNetwork::getProxyName, IWMPNetworkgetProxyName, getProxyName, getProxyName method [Windows Media Player], getProxyName method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_getproxyname, wmp/IWMPNetwork::getProxyName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPNetwork.getProxyName
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::getProxyName


## -description



The <b>getProxyName</b> method retrieves the name of the proxy server being used.




## -parameters




### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="https://msdn.microsoft.com/2672372c-0b42-437e-8b96-83b6e5200fd3">Supported Protocols and File Types</a>.


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




<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/103e0d53-943d-4aba-9db1-20cdc1d75d52">IWMPNetwork::getProxySettings</a>



<a href="https://msdn.microsoft.com/6f484f5b-195c-496d-932e-3e1fdbf873d8">IWMPNetwork::setProxyName</a>
 

 

