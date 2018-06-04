---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
 

 

