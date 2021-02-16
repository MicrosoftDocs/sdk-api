---
UID: NF:qnetwork.IAMNetworkStatus.get_BufferingProgress
title: IAMNetworkStatus::get_BufferingProgress (qnetwork.h)
description: The get_BufferingProgress method retrieves a value indicating the buffering progress.
helpviewer_keywords: ["IAMNetworkStatus interface [DirectShow]","get_BufferingProgress method","IAMNetworkStatus.get_BufferingProgress","IAMNetworkStatus::get_BufferingProgress","IAMNetworkStatusget_BufferingProgress","dshow.iamnetworkstatus_get_bufferingprogress","get_BufferingProgress","get_BufferingProgress method [DirectShow]","get_BufferingProgress method [DirectShow]","IAMNetworkStatus interface","qnetwork/IAMNetworkStatus::get_BufferingProgress"]
old-location: dshow\iamnetworkstatus_get_bufferingprogress.htm
tech.root: dshow
ms.assetid: 76276bdc-1f19-4fb9-8ae9-1edeb5639741
ms.date: 12/05/2018
ms.keywords: IAMNetworkStatus interface [DirectShow],get_BufferingProgress method, IAMNetworkStatus.get_BufferingProgress, IAMNetworkStatus::get_BufferingProgress, IAMNetworkStatusget_BufferingProgress, dshow.iamnetworkstatus_get_bufferingprogress, get_BufferingProgress, get_BufferingProgress method [DirectShow], get_BufferingProgress method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_BufferingProgress
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
 - IAMNetworkStatus::get_BufferingProgress
 - qnetwork/IAMNetworkStatus::get_BufferingProgress
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
 - IAMNetworkStatus.get_BufferingProgress
---

# IAMNetworkStatus::get_BufferingProgress


## -description

The <code>get_BufferingProgress</code> method retrieves a value indicating the buffering progress.

## -parameters

### -param pBufferingProgress

Pointer to a variable that receives a value from 0 to 100, indicating what percentage has completed.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetworkstatus">IAMNetworkStatus Interface</a>