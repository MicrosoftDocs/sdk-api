---
UID: NF:qnetwork.IAMNetShowConfig.get_HTTPProxyPort
title: IAMNetShowConfig::get_HTTPProxyPort (qnetwork.h)
description: The get_HTTPProxyPort method retrieves the HTTP proxy port.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","get_HTTPProxyPort method","IAMNetShowConfig.get_HTTPProxyPort","IAMNetShowConfig::get_HTTPProxyPort","IAMNetShowConfigget_HTTPProxyPort","dshow.iamnetshowconfig_get_httpproxyport","get_HTTPProxyPort","get_HTTPProxyPort method [DirectShow]","get_HTTPProxyPort method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::get_HTTPProxyPort"]
old-location: dshow\iamnetshowconfig_get_httpproxyport.htm
tech.root: dshow
ms.assetid: 4a0325bb-83d6-4fbc-a513-0b6002013a60
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],get_HTTPProxyPort method, IAMNetShowConfig.get_HTTPProxyPort, IAMNetShowConfig::get_HTTPProxyPort, IAMNetShowConfigget_HTTPProxyPort, dshow.iamnetshowconfig_get_httpproxyport, get_HTTPProxyPort, get_HTTPProxyPort method [DirectShow], get_HTTPProxyPort method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_HTTPProxyPort
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
 - IAMNetShowConfig::get_HTTPProxyPort
 - qnetwork/IAMNetShowConfig::get_HTTPProxyPort
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
 - IAMNetShowConfig.get_HTTPProxyPort
---

# IAMNetShowConfig::get_HTTPProxyPort


## -description

The <code>get_HTTPProxyPort</code> method retrieves the HTTP proxy port.

## -parameters

### -param pHTTPProxyPort

Pointer to a variable that receives the port number.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-get_httpproxyhost">IAMNetShowConfig::get_HTTPProxyHost</a>