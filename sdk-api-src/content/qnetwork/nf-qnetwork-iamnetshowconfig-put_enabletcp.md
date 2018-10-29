---
UID: NF:qnetwork.IAMNetShowConfig.put_EnableTCP
title: IAMNetShowConfig::put_EnableTCP
author: windows-sdk-content
description: The put_EnableTCP method enables or disables TCP-based streaming.
old-location: dshow\iamnetshowconfig_put_enabletcp.htm
tech.root: DirectShow
ms.assetid: 8e875901-7ccb-4aa5-b283-f75b791e85f1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],put_EnableTCP method, IAMNetShowConfig.put_EnableTCP, IAMNetShowConfig::put_EnableTCP, IAMNetShowConfigput_EnableTCP, dshow.iamnetshowconfig_put_enabletcp, put_EnableTCP, put_EnableTCP method [DirectShow], put_EnableTCP method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_EnableTCP
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAMNetShowConfig.put_EnableTCP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMNetShowConfig::put_EnableTCP


## -description



The <code>put_EnableTCP</code> method enables or disables TCP-based streaming.




## -parameters




### -param EnableTCP

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
<td>Enable TCP-based streaming.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable TCP-based streaming.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/611b43dc-7f6d-404e-90a4-b109b9475fb6">IAMNetShowConfig Interface</a>



<a href="https://msdn.microsoft.com/2573573e-97e0-4ed4-b702-8c54ef47c5f4">IAMNetShowConfig::put_EnableUDP</a>
 

 

