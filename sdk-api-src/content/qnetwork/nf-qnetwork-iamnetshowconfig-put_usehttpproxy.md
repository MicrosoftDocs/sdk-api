---
UID: NF:qnetwork.IAMNetShowConfig.put_UseHTTPProxy
title: IAMNetShowConfig::put_UseHTTPProxy (qnetwork.h)
author: windows-sdk-content
description: The put_UseHTTPProxy method specifies whether to use an HTTP proxy server.
old-location: dshow\iamnetshowconfig_put_usehttpproxy.htm
tech.root: DirectShow
ms.assetid: 4be1ca01-49c6-4b1e-8fb6-41e598fd157f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],put_UseHTTPProxy method, IAMNetShowConfig.put_UseHTTPProxy, IAMNetShowConfig::put_UseHTTPProxy, IAMNetShowConfigput_UseHTTPProxy, dshow.iamnetshowconfig_put_usehttpproxy, put_UseHTTPProxy, put_UseHTTPProxy method [DirectShow], put_UseHTTPProxy method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_UseHTTPProxy
ms.topic: method
req.header: qnetwork.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowConfig.put_UseHTTPProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMNetShowConfig::put_UseHTTPProxy


## -description



The <code>put_UseHTTPProxy</code> method specifies whether to use an HTTP proxy server.




## -parameters




### -param UseHTTPProxy

Specify one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Use an HTTP proxy server.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Do not use an HTTP proxy server.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd319696(v=VS.85).aspx">IAMNetShowConfig Interface</a>
 

 

