---
UID: NF:qnetwork.IAMNetShowConfig.put_EnableTCP
title: IAMNetShowConfig::put_EnableTCP (qnetwork.h)
description: The put_EnableTCP method enables or disables TCP-based streaming.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","put_EnableTCP method","IAMNetShowConfig.put_EnableTCP","IAMNetShowConfig::put_EnableTCP","IAMNetShowConfigput_EnableTCP","dshow.iamnetshowconfig_put_enabletcp","put_EnableTCP","put_EnableTCP method [DirectShow]","put_EnableTCP method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::put_EnableTCP"]
old-location: dshow\iamnetshowconfig_put_enabletcp.htm
tech.root: dshow
ms.assetid: 8e875901-7ccb-4aa5-b283-f75b791e85f1
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],put_EnableTCP method, IAMNetShowConfig.put_EnableTCP, IAMNetShowConfig::put_EnableTCP, IAMNetShowConfigput_EnableTCP, dshow.iamnetshowconfig_put_enabletcp, put_EnableTCP, put_EnableTCP method [DirectShow], put_EnableTCP method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_EnableTCP
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMNetShowConfig::put_EnableTCP
 - qnetwork/IAMNetShowConfig::put_EnableTCP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowConfig.put_EnableTCP
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

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-put_enableudp">IAMNetShowConfig::put_EnableUDP</a>