---
UID: NF:wmp.IWMPNetwork.getProxySettings
title: IWMPNetwork::getProxySettings (wmp.h)
author: windows-sdk-content
description: The getProxySettings method retrieves the proxy setting for a given protocol.
old-location: wmp\iwmpnetwork_getproxysettings.htm
tech.root: WMP
ms.assetid: 103e0d53-943d-4aba-9db1-20cdc1d75d52
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],getProxySettings method, IWMPNetwork.getProxySettings, IWMPNetwork::getProxySettings, IWMPNetworkgetProxySettings, getProxySettings, getProxySettings method [Windows Media Player], getProxySettings method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_getproxysettings, wmp/IWMPNetwork::getProxySettings
ms.topic: method
f1_keywords: 
 - "wmp/IWMPNetwork.getProxySettings"
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
 - IWMPNetwork.getProxySettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPNetwork::getProxySettings


## -description



The <b>getProxySettings</b> method retrieves the proxy setting for a given protocol.




## -parameters




### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="https://docs.microsoft.com/windows/desktop/WMP/supported-protocols-and-file-types">Supported Protocols and File Types</a>.


### -param plProxySetting [out]

Pointer to a <b>long</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>A proxy server is not being used.</td>
</tr>
<tr>
<td>1</td>
<td>The proxy settings for the current browser are being used (only valid for HTTP).</td>
</tr>
<tr>
<td>2</td>
<td>The manually specified proxy settings are being used.</td>
</tr>
<tr>
<td>3</td>
<td>The proxy settings are being auto-detected.</td>
</tr>
</table>
 


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



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-setproxysettings">IWMPNetwork::setProxySettings</a>
 

 

