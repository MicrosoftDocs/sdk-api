---
UID: NF:rtworkq.RtwqAddPeriodicCallback
title: RtwqAddPeriodicCallback function (rtworkq.h)
description: Sets a callback function to be called at a fixed interval. (RtwqAddPeriodicCallback)
helpviewer_keywords: ["RtwqAddPeriodicCallback","RtwqAddPeriodicCallback function","base.rtwqaddperiodiccallback","rtworkq/RtwqAddPeriodicCallback"]
old-location: base\rtwqaddperiodiccallback.htm
tech.root: backup
ms.assetid: 5f472e42-7c62-462a-91a8-240c395ad765
ms.date: 12/05/2018
ms.keywords: RtwqAddPeriodicCallback, RtwqAddPeriodicCallback function, base.rtwqaddperiodiccallback, rtworkq/RtwqAddPeriodicCallback
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtwqAddPeriodicCallback
 - rtworkq/RtwqAddPeriodicCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqAddPeriodicCallback
---

# RtwqAddPeriodicCallback function


## -description

Sets a callback function to be called at a fixed interval.

## -parameters

### -param Callback [in]

Pointer to the callback function.

### -param context

Pointer to a caller-provided object that implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, or <b>NULL</b>. This parameter is passed to the callback function.

### -param key [out, optional]

Receives a key that can be used to cancel the callback. To cancel the callback, call <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqremoveperiodiccallback">RtwqRemovePeriodicCallback</a> and pass this key as the <i>dwKey</i> parameter.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
