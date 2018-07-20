---
UID: NF:qnetwork.IAMNetShowConfig.put_EnableHTTP
title: IAMNetShowConfig::put_EnableHTTP
author: windows-sdk-content
description: The put_EnableHTTP method enables or disables HTTP-based streaming.
old-location: dshow\iamnetshowconfig_put_enablehttp.htm
old-project: DirectShow
ms.assetid: 162a581d-9697-4a6e-aedc-ec1ebc28a867
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],put_EnableHTTP method, IAMNetShowConfig.put_EnableHTTP, IAMNetShowConfig::put_EnableHTTP, IAMNetShowConfigput_EnableHTTP, dshow.iamnetshowconfig_put_enablehttp, put_EnableHTTP, put_EnableHTTP method [DirectShow], put_EnableHTTP method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_EnableHTTP
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowConfig.put_EnableHTTP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAMNetShowConfig::put_EnableHTTP


## -description



The <code>put_EnableHTTP</code> method enables or disables HTTP-based streaming.




## -parameters




### -param EnableHTTP

Specify one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Enable HTTP-based streaming.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable HTTP-based streaming.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/611b43dc-7f6d-404e-90a4-b109b9475fb6">IAMNetShowConfig Interface</a>
 

 

