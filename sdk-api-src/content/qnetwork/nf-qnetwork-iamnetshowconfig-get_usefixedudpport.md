---
UID: NF:qnetwork.IAMNetShowConfig.get_UseFixedUDPPort
title: IAMNetShowConfig::get_UseFixedUDPPort (qnetwork.h)
description: The get_UseFixedUDPPort method queries whether the filter should use the fixed UDP port.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","get_UseFixedUDPPort method","IAMNetShowConfig.get_UseFixedUDPPort","IAMNetShowConfig::get_UseFixedUDPPort","IAMNetShowConfigget_UseFixedUDPPort","dshow.iamnetshowconfig_get_usefixedudpport","get_UseFixedUDPPort","get_UseFixedUDPPort method [DirectShow]","get_UseFixedUDPPort method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::get_UseFixedUDPPort"]
old-location: dshow\iamnetshowconfig_get_usefixedudpport.htm
tech.root: dshow
ms.assetid: 0a4b1f3b-c630-4820-a9d1-0e93f295b7f7
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],get_UseFixedUDPPort method, IAMNetShowConfig.get_UseFixedUDPPort, IAMNetShowConfig::get_UseFixedUDPPort, IAMNetShowConfigget_UseFixedUDPPort, dshow.iamnetshowconfig_get_usefixedudpport, get_UseFixedUDPPort, get_UseFixedUDPPort method [DirectShow], get_UseFixedUDPPort method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_UseFixedUDPPort
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
 - IAMNetShowConfig::get_UseFixedUDPPort
 - qnetwork/IAMNetShowConfig::get_UseFixedUDPPort
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
 - IAMNetShowConfig.get_UseFixedUDPPort
---

# IAMNetShowConfig::get_UseFixedUDPPort


## -description

The <code>get_UseFixedUDPPort</code> method queries whether the filter should use the fixed UDP port.

## -parameters

### -param pUseFixedUDPPort

Pointer to a variable that receives a Boolean value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-get_fixedudpport">IAMNetShowConfig::get_FixedUDPPort</a>