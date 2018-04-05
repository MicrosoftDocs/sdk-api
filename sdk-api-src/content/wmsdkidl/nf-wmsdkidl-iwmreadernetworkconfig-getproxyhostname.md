---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetProxyHostName
title: IWMReaderNetworkConfig::GetProxyHostName method
author: windows-driver-content
description: The GetProxyHostName method retrieves the name of the host to use as the proxy.
old-location: wmformat\iwmreadernetworkconfig_getproxyhostname.htm
old-project: wmformat
ms.assetid: a7411ed6-90ee-450c-bb06-408469036d22
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetProxyHostName method [windows Media Format], GetProxyHostName method [windows Media Format], IWMReaderNetworkConfig interface, GetProxyHostName,IWMReaderNetworkConfig.GetProxyHostName, IWMReaderNetworkConfig, IWMReaderNetworkConfig interface [windows Media Format], GetProxyHostName method, IWMReaderNetworkConfig::GetProxyHostName, IWMReaderNetworkConfigGetProxyHostName, wmformat.iwmreadernetworkconfig_getproxyhostname, wmsdkidl/IWMReaderNetworkConfig::GetProxyHostName
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
-	IWMReaderNetworkConfig.GetProxyHostName
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::GetProxyHostName method


## -description



The <b>GetProxyHostName</b> method retrieves the name of the host to use as the proxy.




## -parameters




### -param pwszProtocol [in]

Pointer to a string that contains a protocol name, such as "http" or "mms". The string is not case-sensitive.


### -param pwszHostName [out]

Pointer to a buffer that receives the name of the proxy server host. The returned value applies only to the protocol specified in <i>pwszProtocol</i>; the reader object supports separate settings for each protocol.


### -param pcchHostName [in, out]

On input, pointer to a variable specifying the size of <i>pwszHostName</i>, in characters. On output, the variable contains the length of the string, including the terminating <b>null</b> character.


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
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The size of the buffer passed in is not large enough to hold the return string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> or invalid argument passed in.

</td>
</tr>
</table>
 




## -remarks



Call this method twice. The first time, pass <b>NULL</b> as the value for <i>pwszHostName</i>. The method returns the size of the string in the <i>pcchHostName</i> parameter. Allocate the required amount of memory for the string and call the method again. This time, pass a pointer to the allocated buffer in the <i>pwszHostName</i> parameter.

The host name is ignored if the proxy setting is WMT_PROXY_SETTING_AUTO or WMT_PROXY_SETTING_BROWSER.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/5638a5d6-30f3-43eb-b054-cab85948796c">IWMReaderNetworkConfig::SetProxyHostName</a>



<a href="https://msdn.microsoft.com/fe5bc4f2-860a-42e8-b9f1-cd3d8af619c2">IWMReaderNetworkConfig::SetProxySettings</a>
 

 

