---
UID: NF:qnetwork.IAMNetShowConfig.put_EnableUDP
title: IAMNetShowConfig::put_EnableUDP (qnetwork.h)

description: The put_EnableUDP method enables or disablles UDP-based streaming.
old-location: dshow\iamnetshowconfig_put_enableudp.htm
tech.root: DirectShow
ms.assetid: 2573573e-97e0-4ed4-b702-8c54ef47c5f4

ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],put_EnableUDP method, IAMNetShowConfig.put_EnableUDP, IAMNetShowConfig::put_EnableUDP, IAMNetShowConfigput_EnableUDP, dshow.iamnetshowconfig_put_enableudp, put_EnableUDP, put_EnableUDP method [DirectShow], put_EnableUDP method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_EnableUDP
ms.topic: method
f1_keywords: 
 - "qnetwork/IAMNetShowConfig.put_EnableUDP"
dev_langs:
 - c++
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
 - IAMNetShowConfig.put_EnableUDP
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMNetShowConfig::put_EnableUDP


## -description



The <code>put_EnableUDP</code> method enables or disablles UDP-based streaming.




## -parameters




### -param EnableUDP

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
<td>Enable UDP-based streaming.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable UDP-based streaming.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-put_enabletcp">IAMNetShowConfig::put_EnableTCP</a>
 

 

