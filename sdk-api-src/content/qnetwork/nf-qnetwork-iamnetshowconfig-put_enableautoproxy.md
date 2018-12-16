---
UID: NF:qnetwork.IAMNetShowConfig.put_EnableAutoProxy
title: IAMNetShowConfig::put_EnableAutoProxy
author: windows-sdk-content
description: The put_EnableAutoProxy method enables or disables auto-proxy.
old-location: dshow\iamnetshowconfig_put_enableautoproxy.htm
tech.root: DirectShow
ms.assetid: 2746e4d9-3996-4b06-bbb9-7777de6d0202
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],put_EnableAutoProxy method, IAMNetShowConfig.put_EnableAutoProxy, IAMNetShowConfig::put_EnableAutoProxy, IAMNetShowConfigput_EnableAutoProxy, dshow.iamnetshowconfig_put_enableautoproxy, put_EnableAutoProxy, put_EnableAutoProxy method [DirectShow], put_EnableAutoProxy method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_EnableAutoProxy
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
 - IAMNetShowConfig.put_EnableAutoProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMNetShowConfig::put_EnableAutoProxy


## -description



The <code>put_EnableAutoProxy</code> method enables or disables auto-proxy.




## -parameters




### -param EnableAutoProxy

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
<td>Enable auto-proxy.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable auto-proxy.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd319696(v=VS.85).aspx">IAMNetShowConfig Interface</a>
 

 

