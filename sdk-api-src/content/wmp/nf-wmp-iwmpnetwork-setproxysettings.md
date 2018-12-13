---
UID: NF:wmp.IWMPNetwork.setProxySettings
title: IWMPNetwork::setProxySettings
author: windows-sdk-content
description: The setProxySettings method specifies the proxy setting for a given protocol.
old-location: wmp\iwmpnetwork_setproxysettings.htm
tech.root: WMP
ms.assetid: 3ce07bf8-8521-4240-9859-3bf790ccbf48
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],setProxySettings method, IWMPNetwork.setProxySettings, IWMPNetwork::setProxySettings, IWMPNetworksetProxySettings, setProxySettings, setProxySettings method [Windows Media Player], setProxySettings method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_setproxysettings, wmp/IWMPNetwork::setProxySettings
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
 - IWMPNetwork.setProxySettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPNetwork::setProxySettings


## -description



The <b>setProxySettings</b> method specifies the proxy setting for a given protocol.




## -parameters




### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="https://msdn.microsoft.com/2672372c-0b42-437e-8b96-83b6e5200fd3">Supported Protocols and File Types</a>.


### -param lProxySetting [in]

<b>long</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Do not use a proxy server.</td>
</tr>
<tr>
<td>1</td>
<td>Use the proxy settings of the current browser (only valid for HTTP).</td>
</tr>
<tr>
<td>2</td>
<td>Use the manually specified proxy settings.</td>
</tr>
<tr>
<td>3</td>
<td>Auto-detect the proxy settings.</td>
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

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563461(v=VS.85).aspx">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563467(v=VS.85).aspx">IWMPNetwork::getProxySettings</a>
 

 

