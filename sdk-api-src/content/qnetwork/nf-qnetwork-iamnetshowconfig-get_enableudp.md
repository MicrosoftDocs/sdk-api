---
UID: NF:qnetwork.IAMNetShowConfig.get_EnableUDP
title: IAMNetShowConfig::get_EnableUDP (qnetwork.h)
description: The get_EnableUDP method queries whether UDP-based streaming is enabled.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","get_EnableUDP method","IAMNetShowConfig.get_EnableUDP","IAMNetShowConfig::get_EnableUDP","IAMNetShowConfigget_EnableUDP","dshow.iamnetshowconfig_get_enableudp","get_EnableUDP","get_EnableUDP method [DirectShow]","get_EnableUDP method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::get_EnableUDP"]
old-location: dshow\iamnetshowconfig_get_enableudp.htm
tech.root: dshow
ms.assetid: 95c689c9-34f6-49b2-bd3b-0f68a110c4f2
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],get_EnableUDP method, IAMNetShowConfig.get_EnableUDP, IAMNetShowConfig::get_EnableUDP, IAMNetShowConfigget_EnableUDP, dshow.iamnetshowconfig_get_enableudp, get_EnableUDP, get_EnableUDP method [DirectShow], get_EnableUDP method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_EnableUDP
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
 - IAMNetShowConfig::get_EnableUDP
 - qnetwork/IAMNetShowConfig::get_EnableUDP
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
 - IAMNetShowConfig.get_EnableUDP
---

# IAMNetShowConfig::get_EnableUDP


## -description

The <code>get_EnableUDP</code> method queries whether UDP-based streaming is enabled.

## -parameters

### -param pEnableUDP

Pointer to a variable that receives a Boolean value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-get_enabletcp">IAMNetShowConfig::get_EnableTCP</a>