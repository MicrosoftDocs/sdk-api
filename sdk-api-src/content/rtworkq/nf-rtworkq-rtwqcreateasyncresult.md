---
UID: NF:rtworkq.RtwqCreateAsyncResult
title: RtwqCreateAsyncResult function
author: windows-sdk-content
description: Creates an asynchronous result object. Use this function if you are implementing an asynchronous method.
old-location: base\rtwqcreateasyncresult.htm
tech.root: procthread
ms.assetid: ba8e888a-5bd6-4624-94a6-2f2ce0a080d1
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: RtwqCreateAsyncResult, RtwqCreateAsyncResult function, base.rtwqcreateasyncresult, rtworkq/RtwqCreateAsyncResult
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
 - RtwqCreateAsyncResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtwqCreateAsyncResult function


## -description



Creates an asynchronous result object. Use this function if you are implementing an asynchronous method.




## -parameters




### -param appObject [in]

Pointer to the object stored in the asynchronous result. This pointer is returned by the <a href="https://msdn.microsoft.com/EF872EDD-4263-4835-81E4-0A61F18E9202">IRtwqAsyncResult::GetObject</a> method. This parameter can be <b>NULL</b>.


### -param callback [in]

Pointer to the <a href="https://msdn.microsoft.com/E595C072-98F8-4231-9C8F-A8393D751DE6">IRtwqAsyncCallback</a> interface. This interface is implemented by the caller of the asynchronous method.


### -param appState [in]

Pointer to the <b>IUnknown</b> interface of a state object. This value is provided by the caller of the asynchronous method. This parameter can be <b>NULL</b>.


### -param asyncResult [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/AB23282D-D731-48EE-AF55-CC5A513EBA33">IRtwqAsyncResult</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To invoke the callback specified in <i>pCallback</i>, call the <a href="https://msdn.microsoft.com/ba1ac638-b21d-4a0e-8599-b572b5ef2fa6">RtwqInvokeCallback</a> function.



