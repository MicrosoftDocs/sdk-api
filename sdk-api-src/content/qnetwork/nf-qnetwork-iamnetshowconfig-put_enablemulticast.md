---
UID: NF:qnetwork.IAMNetShowConfig.put_EnableMulticast
title: IAMNetShowConfig::put_EnableMulticast (qnetwork.h)
description: The put_EnableMulticast method enables or disables multicast-based streaming.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","put_EnableMulticast method","IAMNetShowConfig.put_EnableMulticast","IAMNetShowConfig::put_EnableMulticast","IAMNetShowConfigput_EnableMulticast","dshow.iamnetshowconfig_put_enablemulticast","put_EnableMulticast","put_EnableMulticast method [DirectShow]","put_EnableMulticast method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::put_EnableMulticast"]
old-location: dshow\iamnetshowconfig_put_enablemulticast.htm
tech.root: dshow
ms.assetid: 8415560c-0dc8-4d37-b584-9e278542cf15
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],put_EnableMulticast method, IAMNetShowConfig.put_EnableMulticast, IAMNetShowConfig::put_EnableMulticast, IAMNetShowConfigput_EnableMulticast, dshow.iamnetshowconfig_put_enablemulticast, put_EnableMulticast, put_EnableMulticast method [DirectShow], put_EnableMulticast method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_EnableMulticast
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
 - IAMNetShowConfig::put_EnableMulticast
 - qnetwork/IAMNetShowConfig::put_EnableMulticast
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
 - IAMNetShowConfig.put_EnableMulticast
---

# IAMNetShowConfig::put_EnableMulticast


## -description

The <code>put_EnableMulticast</code> method enables or disables multicast-based streaming.

## -parameters

### -param EnableMulticast

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
<td>Enable multicast-based streaming.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable multicast-based streaming.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>