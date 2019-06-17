---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetProxySettings
title: IWMReaderNetworkConfig::SetProxySettings (wmsdkidl.h)
author: windows-sdk-content
description: The SetProxySettings method specifies the proxy settings.
old-location: wmformat\iwmreadernetworkconfig_setproxysettings.htm
tech.root: wmformat
ms.assetid: fe5bc4f2-860a-42e8-b9f1-cd3d8af619c2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetProxySettings method, IWMReaderNetworkConfig.SetProxySettings, IWMReaderNetworkConfig::SetProxySettings, IWMReaderNetworkConfigSetProxySettings, SetProxySettings, SetProxySettings method [windows Media Format], SetProxySettings method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setproxysettings, wmsdkidl/IWMReaderNetworkConfig::SetProxySettings
ms.topic: method
f1_keywords: ["wmsdkidl/IWMReaderNetworkConfig.SetProxySettings"]
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
 - IWMReaderNetworkConfig.SetProxySettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderNetworkConfig::SetProxySettings


## -description



The <b>SetProxySettings</b> method specifies the proxy settings.




## -parameters




### -param pwszProtocol [in]

Pointer to a wide-character null-terminated string containing the protocol name. Supported names are HTTP and MMS.


### -param ProxySetting [in]

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_proxy_settings">WMT_PROXY_SETTINGS</a> enumeration type.


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



Setting the protocol to WMT_PROXY_SETTING_MANUAL causes the reader to use the proxy settings from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyhostname">SetProxyHostName</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyport">SetProxyPort</a>. Setting it to WMT_PROXY_SETTING_AUTO uses Web Proxy Auto-Detect mechanisms to dynamically determine the appropriate proxy based on the specified URL. Setting the protocol to WMT_PROXY_SETTING_BROWSER is valid only for HTTP URLs, and causes the reader to use the proxy settings that are configured in the browser.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxysettings">IWMReaderNetworkConfig::GetProxySettings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyhostname">IWMReaderNetworkConfig::SetProxyHostName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyport">IWMReaderNetworkConfig::SetProxyPort</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_proxy_settings">WMT_PROXY_SETTINGS</a>
 

 

