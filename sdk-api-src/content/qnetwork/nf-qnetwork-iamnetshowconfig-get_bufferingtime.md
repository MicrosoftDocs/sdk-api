---
UID: NF:qnetwork.IAMNetShowConfig.get_BufferingTime
title: IAMNetShowConfig::get_BufferingTime (qnetwork.h)
description: The get_BufferingTime method retrieves the buffering time.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","get_BufferingTime method","IAMNetShowConfig.get_BufferingTime","IAMNetShowConfig::get_BufferingTime","IAMNetShowConfigget_BufferingTime","dshow.iamnetshowconfig_get_bufferingtime","get_BufferingTime","get_BufferingTime method [DirectShow]","get_BufferingTime method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::get_BufferingTime"]
old-location: dshow\iamnetshowconfig_get_bufferingtime.htm
tech.root: dshow
ms.assetid: 8594f8dd-9545-4e6d-b1d7-9a278dcb4129
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],get_BufferingTime method, IAMNetShowConfig.get_BufferingTime, IAMNetShowConfig::get_BufferingTime, IAMNetShowConfigget_BufferingTime, dshow.iamnetshowconfig_get_bufferingtime, get_BufferingTime, get_BufferingTime method [DirectShow], get_BufferingTime method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_BufferingTime
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
 - IAMNetShowConfig::get_BufferingTime
 - qnetwork/IAMNetShowConfig::get_BufferingTime
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
 - IAMNetShowConfig.get_BufferingTime
---

# IAMNetShowConfig::get_BufferingTime


## -description

The <code>get_BufferingTime</code> method retrieves the buffering time.

## -parameters

### -param pBufferingTime

Pointer that receives the buffering time, in seconds.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>