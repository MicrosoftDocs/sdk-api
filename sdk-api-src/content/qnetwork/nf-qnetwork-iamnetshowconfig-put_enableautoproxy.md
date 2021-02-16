---
UID: NF:qnetwork.IAMNetShowConfig.put_EnableAutoProxy
title: IAMNetShowConfig::put_EnableAutoProxy (qnetwork.h)
description: The put_EnableAutoProxy method enables or disables auto-proxy.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","put_EnableAutoProxy method","IAMNetShowConfig.put_EnableAutoProxy","IAMNetShowConfig::put_EnableAutoProxy","IAMNetShowConfigput_EnableAutoProxy","dshow.iamnetshowconfig_put_enableautoproxy","put_EnableAutoProxy","put_EnableAutoProxy method [DirectShow]","put_EnableAutoProxy method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::put_EnableAutoProxy"]
old-location: dshow\iamnetshowconfig_put_enableautoproxy.htm
tech.root: dshow
ms.assetid: 2746e4d9-3996-4b06-bbb9-7777de6d0202
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],put_EnableAutoProxy method, IAMNetShowConfig.put_EnableAutoProxy, IAMNetShowConfig::put_EnableAutoProxy, IAMNetShowConfigput_EnableAutoProxy, dshow.iamnetshowconfig_put_enableautoproxy, put_EnableAutoProxy, put_EnableAutoProxy method [DirectShow], put_EnableAutoProxy method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_EnableAutoProxy
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
 - IAMNetShowConfig::put_EnableAutoProxy
 - qnetwork/IAMNetShowConfig::put_EnableAutoProxy
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
 - IAMNetShowConfig.put_EnableAutoProxy
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

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>