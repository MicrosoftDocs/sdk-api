---
UID: NF:wmp.IWMPNetwork.getProxyPort
title: IWMPNetwork::getProxyPort method
author: windows-driver-content
description: The getProxyPort method retrieves the proxy port being used.
old-location: wmp\iwmpnetwork_getproxyport.htm
old-project: WMP
ms.assetid: 0d636e61-a5c1-495a-8d1d-ce2937dd3f18
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPNetwork, IWMPNetwork interface [Windows Media Player], getProxyPort method, IWMPNetwork::getProxyPort, IWMPNetworkgetProxyPort, getProxyPort method [Windows Media Player], getProxyPort method [Windows Media Player], IWMPNetwork interface, getProxyPort,IWMPNetwork.getProxyPort, wmp.iwmpnetwork_getproxyport, wmp/IWMPNetwork::getProxyPort
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPNetwork.getProxyPort
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::getProxyPort method


## -description



The <b>getProxyPort</b> method retrieves the proxy port being used.




## -parameters




### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="https://msdn.microsoft.com/2672372c-0b42-437e-8b96-83b6e5200fd3">Supported Protocols and File Types</a>.


### -param lProxyPort






#### - plProxyPort [out]

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




<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/103e0d53-943d-4aba-9db1-20cdc1d75d52">IWMPNetwork::getProxySettings</a>



<a href="https://msdn.microsoft.com/36b7290d-c359-45bb-b77b-46b696e9edcf">IWMPNetwork::setProxyPort</a>
 

 

