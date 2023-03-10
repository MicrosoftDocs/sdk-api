---
UID: NF:rtworkq.RtwqRemovePeriodicCallback
title: RtwqRemovePeriodicCallback function (rtworkq.h)
description: Cancels a callback function that was set by the RtwqAddPeriodicCallback function.
helpviewer_keywords: ["RtwqRemovePeriodicCallback","RtwqRemovePeriodicCallback function","base.rtwqremoveperiodiccallback","rtworkq/RtwqRemovePeriodicCallback"]
old-location: base\rtwqremoveperiodiccallback.htm
tech.root: backup
ms.assetid: 308910e3-dae8-4f23-9782-adf2996a58aa
ms.date: 12/05/2018
ms.keywords: RtwqRemovePeriodicCallback, RtwqRemovePeriodicCallback function, base.rtwqremoveperiodiccallback, rtworkq/RtwqRemovePeriodicCallback
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
 - RtwqRemovePeriodicCallback
 - rtworkq/RtwqRemovePeriodicCallback
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
 - RtwqRemovePeriodicCallback
---

# RtwqRemovePeriodicCallback function


## -description

Cancels a callback function that was set by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqaddperiodiccallback">RtwqAddPeriodicCallback</a> function.

## -parameters

### -param dwKey [in]

Key that identifies the callback. This value is retrieved by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqaddperiodiccallback">RtwqAddPeriodicCallback</a> function.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.