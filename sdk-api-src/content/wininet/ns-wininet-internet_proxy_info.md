---
UID: NS:wininet.INTERNET_PROXY_INFO
title: INTERNET_PROXY_INFO
author: windows-driver-content
description: Contains information that is supplied with the INTERNET_OPTION_PROXY value to get or set proxy information on a handle obtained from a call to the InternetOpen function.
old-location: wininet\internet_proxy_info.htm
old-project: WinInet
ms.assetid: f2431800-dbcc-4933-87f5-2d08ca22ad9c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "*LPINTERNET_PROXY_INFO, INTERNET_OPEN_TYPE_DIRECT, INTERNET_OPEN_TYPE_PRECONFIG, INTERNET_OPEN_TYPE_PROXY, INTERNET_PROXY_INFO, INTERNET_PROXY_INFO structure [WinINet], LPINTERNET_PROXY_INFO, LPINTERNET_PROXY_INFO structure pointer [WinINet], _inet_internet_proxy_info_structure, wininet.internet_proxy_info, wininet/ LPINTERNET_PROXY_INFO, wininet/INTERNET_PROXY_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: INTERNET_PROXY_INFO, *LPINTERNET_PROXY_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wininet.h
api_name:
-	INTERNET_PROXY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# INTERNET_PROXY_INFO structure


## -description


Contains information that is supplied with the INTERNET_OPTION_PROXY value to get or set proxy information on a handle obtained from a call to the 
<a href="https://msdn.microsoft.com/9ec087c9-d484-4763-a527-2ea5c1a0cf28">InternetOpen</a> function. 


## -struct-fields




### -field dwAccessType

Access type. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_OPEN_TYPE_DIRECT"></a><a id="internet_open_type_direct"></a><dl>
<dt><b>INTERNET_OPEN_TYPE_DIRECT</b></dt>
</dl>
</td>
<td width="60%">
Internet accessed through a direct connection. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_OPEN_TYPE_PRECONFIG"></a><a id="internet_open_type_preconfig"></a><dl>
<dt><b>INTERNET_OPEN_TYPE_PRECONFIG</b></dt>
</dl>
</td>
<td width="60%">
Applies only when setting proxy information. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_OPEN_TYPE_PROXY"></a><a id="internet_open_type_proxy"></a><dl>
<dt><b>INTERNET_OPEN_TYPE_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Internet accessed using a proxy. 

</td>
</tr>
</table>
 


### -field lpszProxy

Pointer to a string that contains the proxy server list. 


### -field lpszProxyBypass

Pointer to a string that contains the proxy bypass list. 


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a>



<a href="https://msdn.microsoft.com/578c7130-7426-4a2e-ae0f-ed8a84449b06">InternetSetOption</a>
 

 

