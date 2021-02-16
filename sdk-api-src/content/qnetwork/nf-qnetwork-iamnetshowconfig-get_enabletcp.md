---
UID: NF:qnetwork.IAMNetShowConfig.get_EnableTCP
title: IAMNetShowConfig::get_EnableTCP (qnetwork.h)
description: The get_EnableTCP method queries whether TCP-based streaming is enabled.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","get_EnableTCP method","IAMNetShowConfig.get_EnableTCP","IAMNetShowConfig::get_EnableTCP","IAMNetShowConfigget_EnableTCP","dshow.iamnetshowconfig_get_enabletcp","get_EnableTCP","get_EnableTCP method [DirectShow]","get_EnableTCP method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::get_EnableTCP"]
old-location: dshow\iamnetshowconfig_get_enabletcp.htm
tech.root: dshow
ms.assetid: b4282f84-e05b-407f-9425-0690783957c4
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],get_EnableTCP method, IAMNetShowConfig.get_EnableTCP, IAMNetShowConfig::get_EnableTCP, IAMNetShowConfigget_EnableTCP, dshow.iamnetshowconfig_get_enabletcp, get_EnableTCP, get_EnableTCP method [DirectShow], get_EnableTCP method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_EnableTCP
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
 - IAMNetShowConfig::get_EnableTCP
 - qnetwork/IAMNetShowConfig::get_EnableTCP
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
 - IAMNetShowConfig.get_EnableTCP
---

# IAMNetShowConfig::get_EnableTCP


## -description

The <code>get_EnableTCP</code> method queries whether TCP-based streaming is enabled.

## -parameters

### -param pEnableTCP

Pointer to a variable that receives a Boolean value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-get_enableudp">IAMNetShowConfig::get_EnableUDP</a>