---
UID: NF:rtworkq.RtwqAddPeriodicCallback
title: RtwqAddPeriodicCallback function
author: windows-sdk-content
description: Sets a callback function to be called at a fixed interval.
old-location: base\rtwqaddperiodiccallback.htm
old-project: ProcThread
ms.assetid: 5f472e42-7c62-462a-91a8-240c395ad765
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: RtwqAddPeriodicCallback, RtwqAddPeriodicCallback function, base.rtwqaddperiodiccallback, rtworkq/RtwqAddPeriodicCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RTWorkQ.dll
api_name:
-	RtwqAddPeriodicCallback
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RtwqAddPeriodicCallback function


## -description


Sets a callback function to be called at a fixed interval.


## -parameters




### -param Callback [in]

Pointer to the callback function. 


### -param context

Pointer to a caller-provided object that implements <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, or <b>NULL</b>. This parameter is passed to the callback function.


### -param key [out, optional]

Receives a key that can be used to cancel the callback. To cancel the callback, call <a href="https://msdn.microsoft.com/308910e3-dae8-4f23-9782-adf2996a58aa">RtwqRemovePeriodicCallback</a> and pass this key as the <i>dwKey</i> parameter.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



