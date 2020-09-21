---
UID: NF:qnetwork.IAMNetShowConfig.get_UseHTTPProxy
title: IAMNetShowConfig::get_UseHTTPProxy (qnetwork.h)
description: The get_UseHTTPProxy method queries whether the filter should use the HTTP proxy server.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","get_UseHTTPProxy method","IAMNetShowConfig.get_UseHTTPProxy","IAMNetShowConfig::get_UseHTTPProxy","IAMNetShowConfigget_UseHTTPProxy","dshow.iamnetshowconfig_get_usehttpproxy","get_UseHTTPProxy","get_UseHTTPProxy method [DirectShow]","get_UseHTTPProxy method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::get_UseHTTPProxy"]
old-location: dshow\iamnetshowconfig_get_usehttpproxy.htm
tech.root: dshow
ms.assetid: 4d51676a-bf14-408c-bc8b-331ce11fc237
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],get_UseHTTPProxy method, IAMNetShowConfig.get_UseHTTPProxy, IAMNetShowConfig::get_UseHTTPProxy, IAMNetShowConfigget_UseHTTPProxy, dshow.iamnetshowconfig_get_usehttpproxy, get_UseHTTPProxy, get_UseHTTPProxy method [DirectShow], get_UseHTTPProxy method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_UseHTTPProxy
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
 - IAMNetShowConfig::get_UseHTTPProxy
 - qnetwork/IAMNetShowConfig::get_UseHTTPProxy
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
 - IAMNetShowConfig.get_UseHTTPProxy
---

# IAMNetShowConfig::get_UseHTTPProxy


## -description

The <code>get_UseHTTPProxy</code> method queries whether the filter should use the HTTP proxy server.

## -parameters

### -param pUseHTTPProxy

Pointer to a variable that receives a Boolean value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>