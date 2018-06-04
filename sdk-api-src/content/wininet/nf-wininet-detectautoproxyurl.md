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

# DetectAutoProxyUrl function


## -description


Attempts to determine the location of a WPAD autoproxy script.


## -parameters




### -param pszAutoProxyUrl

TBD


### -param cchAutoProxyUrl

TBD


### -param dwDetectFlags [in]

Automation detection type. This parameter can be one or both of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROXY_AUTO_DETECT_TYPE_DHCP"></a><a id="proxy_auto_detect_type_dhcp"></a><dl>
<dt><b>PROXY_AUTO_DETECT_TYPE_DHCP</b></dt>
</dl>
</td>
<td width="60%">
Use a Dynamic Host Configuration Protocol (DHCP) search to identify the proxy.

</td>
</tr>
<tr>
<td width="40%"><a id="PROXY_AUTO_DETECT_TYPE_DNS_A"></a><a id="proxy_auto_detect_type_dns_a"></a><dl>
<dt><b>PROXY_AUTO_DETECT_TYPE_DNS_A</b></dt>
</dl>
</td>
<td width="60%">
Use a well qualified name search to identify the proxy.

</td>
</tr>
</table>
 


#### - dwAutoProxyUrlLength [in]

Size of 
the buffer pointed to by <i>lpszAutoProxyUrl</i>, in bytes.


#### - lpszAutoProxyUrl [in, out]

Pointer to a buffer to receive the URL from which a WPAD autoproxy script can be downloaded.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ccb69e89-9407-48ac-bb70-fbc425bd1051">InternetDeInitializeAutoProxyDll</a>



<a href="https://msdn.microsoft.com/5fc0f471-420c-4125-8323-cb1e1e72e43f">InternetGetProxyInfo</a>



<a href="https://msdn.microsoft.com/d55d64cb-ee92-4366-a1bb-f5d421ed81c8">InternetInitializeAutoProxyDll</a>
 

 

