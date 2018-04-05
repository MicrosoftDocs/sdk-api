---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetProxyPort
title: IWMReaderNetworkConfig::GetProxyPort method
author: windows-driver-content
description: The GetProxyPort method retrieves the port number of the proxy server.
old-location: wmformat\iwmreadernetworkconfig_getproxyport.htm
old-project: wmformat
ms.assetid: 042d702e-b4a1-43f6-b2c4-c81922d7c3f2
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetProxyPort method [windows Media Format], GetProxyPort method [windows Media Format], IWMReaderNetworkConfig interface, GetProxyPort,IWMReaderNetworkConfig.GetProxyPort, IWMReaderNetworkConfig, IWMReaderNetworkConfig interface [windows Media Format], GetProxyPort method, IWMReaderNetworkConfig::GetProxyPort, IWMReaderNetworkConfigGetProxyPort, wmformat.iwmreadernetworkconfig_getproxyport, wmsdkidl/IWMReaderNetworkConfig::GetProxyPort
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
-	IWMReaderNetworkConfig.GetProxyPort
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::GetProxyPort method


## -description



The <b>GetProxyPort</b> method retrieves the port number of the proxy server.




## -parameters




### -param pwszProtocol [in]

Pointer to a string that contains a protocol name, such as "http" or "mms". The string is not case-sensitive.


### -param pdwPort [out]

Pointer to a variable that receives the port number. The returned value applies only to the protocol specified in <i>pwszProtocol</i>; the reader object supports separate settings for each protocol.


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
NULL or invalid argument passed in.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/e2f4e8ff-6ac8-45b5-af93-a278bf92a07a">IWMReaderNetworkConfig::SetProxyPort</a>
 

 

