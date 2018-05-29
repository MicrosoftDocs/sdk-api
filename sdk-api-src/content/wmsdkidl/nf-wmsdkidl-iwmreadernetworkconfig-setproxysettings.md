---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetProxySettings
title: IWMReaderNetworkConfig::SetProxySettings
author: windows-sdk-content
description: The SetProxySettings method specifies the proxy settings.
old-location: wmformat\iwmreadernetworkconfig_setproxysettings.htm
old-project: wmformat
ms.assetid: fe5bc4f2-860a-42e8-b9f1-cd3d8af619c2
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetProxySettings method, IWMReaderNetworkConfig.SetProxySettings, IWMReaderNetworkConfig::SetProxySettings, IWMReaderNetworkConfigSetProxySettings, SetProxySettings, SetProxySettings method [windows Media Format], SetProxySettings method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setproxysettings, wmsdkidl/IWMReaderNetworkConfig::SetProxySettings
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderNetworkConfig.SetProxySettings
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::SetProxySettings


## -description



The <b>SetProxySettings</b> method specifies the proxy settings.




## -parameters




### -param pwszProtocol [in]

Pointer to a wide-character null-terminated string containing the protocol name. Supported names are HTTP and MMS.


### -param ProxySetting [in]

A value from the <a href="https://msdn.microsoft.com/a055259e-e207-426c-b6ca-a27bc3d0e88c">WMT_PROXY_SETTINGS</a> enumeration type.


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



Setting the protocol to WMT_PROXY_SETTING_MANUAL causes the reader to use the proxy settings from <a href="https://msdn.microsoft.com/5638a5d6-30f3-43eb-b054-cab85948796c">SetProxyHostName</a> and <a href="https://msdn.microsoft.com/e2f4e8ff-6ac8-45b5-af93-a278bf92a07a">SetProxyPort</a>. Setting it to WMT_PROXY_SETTING_AUTO uses Web Proxy Auto-Detect mechanisms to dynamically determine the appropriate proxy based on the specified URL. Setting the protocol to WMT_PROXY_SETTING_BROWSER is valid only for HTTP URLs, and causes the reader to use the proxy settings that are configured in the browser.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/5fdfc651-05f5-48b3-aeaf-4557c72bc0c0">IWMReaderNetworkConfig::GetProxySettings</a>



<a href="https://msdn.microsoft.com/5638a5d6-30f3-43eb-b054-cab85948796c">IWMReaderNetworkConfig::SetProxyHostName</a>



<a href="https://msdn.microsoft.com/e2f4e8ff-6ac8-45b5-af93-a278bf92a07a">IWMReaderNetworkConfig::SetProxyPort</a>



<a href="https://msdn.microsoft.com/a055259e-e207-426c-b6ca-a27bc3d0e88c">WMT_PROXY_SETTINGS</a>
 

 

