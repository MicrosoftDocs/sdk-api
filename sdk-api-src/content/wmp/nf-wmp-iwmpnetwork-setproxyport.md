---
UID: NF:wmp.IWMPNetwork.setProxyPort
title: IWMPNetwork::setProxyPort
author: windows-sdk-content
description: The setProxyPort method specifies the proxy port to use.
old-location: wmp\iwmpnetwork_setproxyport.htm
old-project: WMP
ms.assetid: 36b7290d-c359-45bb-b77b-46b696e9edcf
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],setProxyPort method, IWMPNetwork.setProxyPort, IWMPNetwork::setProxyPort, IWMPNetworksetProxyPort, setProxyPort, setProxyPort method [Windows Media Player], setProxyPort method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_setproxyport, wmp/IWMPNetwork::setProxyPort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
 - IWMPNetwork.setProxyPort
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::setProxyPort


## -description



The <b>setProxyPort</b> method specifies the proxy port to use.




## -parameters




### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="https://msdn.microsoft.com/2672372c-0b42-437e-8b96-83b6e5200fd3">Supported Protocols and File Types</a>..


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




<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/0d636e61-a5c1-495a-8d1d-ce2937dd3f18">IWMPNetwork::getProxyPort</a>



<a href="https://msdn.microsoft.com/103e0d53-943d-4aba-9db1-20cdc1d75d52">IWMPNetwork::getProxySettings</a>
 

 

