---
UID: NF:rtworkq.RtwqInvokeCallback
title: RtwqInvokeCallback function
author: windows-sdk-content
description: Invokes a callback method to complete an asynchronous operation.
old-location: base\rtwqinvokecallback.htm
tech.root: procthread
ms.assetid: ba1ac638-b21d-4a0e-8599-b572b5ef2fa6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtwqInvokeCallback, RtwqInvokeCallback function, base.rtwqinvokecallback, rtworkq/RtwqInvokeCallback
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqInvokeCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtwqInvokeCallback function


## -description


Invokes a callback method to complete an asynchronous operation.


## -parameters




### -param result

The asynchronous result. To create this object, call <a href="https://msdn.microsoft.com/ba8e888a-5bd6-4624-94a6-2f2ce0a080d1">RtwqCreateAsyncResult</a>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



