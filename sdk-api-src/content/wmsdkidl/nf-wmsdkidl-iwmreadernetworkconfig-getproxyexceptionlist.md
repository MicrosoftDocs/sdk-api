---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetProxyExceptionList
title: IWMReaderNetworkConfig::GetProxyExceptionList
author: windows-sdk-content
description: The GetProxyExceptionList method retrieves the list of computers, domains, or addresses for which the reader object bypasses the proxy server.
old-location: wmformat\iwmreadernetworkconfig_getproxyexceptionlist.htm
old-project: wmformat
ms.assetid: 90cf6e58-8666-4bab-974e-a7e999aeddf1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetProxyExceptionList, GetProxyExceptionList method [windows Media Format], GetProxyExceptionList method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetProxyExceptionList method, IWMReaderNetworkConfig.GetProxyExceptionList, IWMReaderNetworkConfig::GetProxyExceptionList, IWMReaderNetworkConfigGetProxyExceptionList, wmformat.iwmreadernetworkconfig_getproxyexceptionlist, wmsdkidl/IWMReaderNetworkConfig::GetProxyExceptionList
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
-	IWMReaderNetworkConfig.GetProxyExceptionList
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::GetProxyExceptionList


## -description



The <b>GetProxyExceptionList</b> method retrieves the list of computers, domains, or addresses for which the reader object bypasses the proxy server.




## -parameters




### -param pwszProtocol [in]

Pointer to a string that contains a protocol name, such as "http" or "mms". The string is not case-sensitive.


### -param pwszExceptionList [out]

Pointer to a buffer that receives a string containing the exception list. The returned string is a comma-separated list. For more information, see <a href="https://msdn.microsoft.com/1f6c6bb6-3a42-44da-ab80-e72a19b8d272">SetProxyExceptionList</a>. The list applies only to the protocol specified in <i>pwszProtocol</i>; the reader object supports separate settings for each protocol.


### -param pcchExceptionList [in, out]

On input, pointer to a variable specifying the size of the <i>pwszExceptionList</i> buffer, in characters. On output, the variable contains the length of the string, including the terminating <b>null</b> character.


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
<b>NULL</b> or invalid argument passed in.

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
</table>
 




## -remarks



Call this method twice. The first time, pass <b>NULL</b> as the value for <i>pwszExceptionList</i>. The method returns the size of the string in the <i>pcchExceptionList</i> parameter. Allocate the required amount of memory for the string and call the method again. This time, pass a pointer to the allocated buffer in the <i>pwszExceptionList</i> parameter.

For more information, see the Remarks for <a href="https://msdn.microsoft.com/1f6c6bb6-3a42-44da-ab80-e72a19b8d272">SetProxyExceptionList</a>.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/1f6c6bb6-3a42-44da-ab80-e72a19b8d272">IWMReaderNetworkConfig::SetProxyExceptionList</a>
 

 

