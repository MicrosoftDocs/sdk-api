---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetProxyPort
title: IWMReaderNetworkConfig::SetProxyPort (wmsdkidl.h)
author: windows-sdk-content
description: The SetProxyPort method specifies the proxy port.
old-location: wmformat\iwmreadernetworkconfig_setproxyport.htm
tech.root: wmformat
ms.assetid: e2f4e8ff-6ac8-45b5-af93-a278bf92a07a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetProxyPort method, IWMReaderNetworkConfig.SetProxyPort, IWMReaderNetworkConfig::SetProxyPort, IWMReaderNetworkConfigSetProxyPort, SetProxyPort, SetProxyPort method [windows Media Format], SetProxyPort method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setproxyport, wmsdkidl/IWMReaderNetworkConfig::SetProxyPort
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
 - IWMReaderNetworkConfig.SetProxyPort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig::SetProxyPort


## -description



The <b>SetProxyPort</b> method specifies the proxy port.




## -parameters




### -param pwszProtocol [in]

Pointer to a wide-character null-terminated string containing the protocol.


### -param dwPort [in]

<b>DWORD</b> containing the name of the port.


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



By default, the port numbers are 1755 for MMS and 80 for HTTP. The correct port number must be set if a port is required. It is not required if the proxy setting is WMT_PROXY_SETTING_AUTO or WMT_PROXY_SETTING_BROWSER.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743504(v=VS.85).aspx">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743533(v=VS.85).aspx">IWMReaderNetworkConfig::GetProxyPort</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743550(v=VS.85).aspx">IWMReaderNetworkConfig::SetProxySettings</a>
 

 

