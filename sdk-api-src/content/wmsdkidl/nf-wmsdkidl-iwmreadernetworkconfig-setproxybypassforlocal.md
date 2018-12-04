---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetProxyBypassForLocal
title: IWMReaderNetworkConfig::SetProxyBypassForLocal
author: windows-sdk-content
description: The SetProxyBypassForLocal method specifies the configuration setting for bypassing the proxy for local hosts.
old-location: wmformat\iwmreadernetworkconfig_setproxybypassforlocal.htm
tech.root: wmformat
ms.assetid: 4a012718-a815-4e01-97f8-69ed2ba881ea
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetProxyBypassForLocal method, IWMReaderNetworkConfig.SetProxyBypassForLocal, IWMReaderNetworkConfig::SetProxyBypassForLocal, IWMReaderNetworkConfigSetProxyBypassForLocal, SetProxyBypassForLocal, SetProxyBypassForLocal method [windows Media Format], SetProxyBypassForLocal method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setproxybypassforlocal, wmsdkidl/IWMReaderNetworkConfig::SetProxyBypassForLocal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderNetworkConfig.SetProxyBypassForLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig::SetProxyBypassForLocal


## -description



The <b>SetProxyBypassForLocal</b> method specifies the configuration setting for bypassing the proxy for local hosts.




## -parameters




### -param pwszProtocol [in]

Pointer to a wide-character null-terminated string containing the protocol.


### -param fBypassForLocal [in]

Boolean value that is True if bypassing the proxy for local hosts is to be enabled (implying that the origin server is on the local network).


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL or invalid argument passed in.

</td>
</tr>
</table>
 




## -remarks



This setting is used only when the proxy setting is WMT_PROXY_SETTING_MANUAL. If the proxy setting is WMT_PROXY_SETTING_BROWSER, the local bypass flag setting in the browser is used instead.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/5e960fa9-d71c-4a13-9210-8a2a86e9989c">IWMReaderNetworkConfig::GetProxyBypassForLocal</a>



<a href="https://msdn.microsoft.com/fe5bc4f2-860a-42e8-b9f1-cd3d8af619c2">IWMReaderNetworkConfig::SetProxySettings</a>
 

 

