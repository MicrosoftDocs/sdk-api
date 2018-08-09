---
UID: NF:rtworkq.RtwqScheduleWorkItem
title: RtwqScheduleWorkItem function
author: windows-sdk-content
description: Schedules an asynchronous operation to be completed after a specified interval.
old-location: base\rtwqscheduleworkitem.htm
old-project: procthread
ms.assetid: cfc22cfb-44fc-441b-826c-61f72cb0bd68
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RtwqScheduleWorkItem, RtwqScheduleWorkItem function, base.rtwqscheduleworkitem, rtworkq/RtwqScheduleWorkItem
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
tech.root: 
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqScheduleWorkItem
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: ADAM
---

# RtwqScheduleWorkItem function


## -description


Schedules an asynchronous operation to be completed after a specified interval.


## -parameters




### -param result [in]

A pointer to the callback. The caller must implement this interface.


### -param Timeout [in]

Time-out interval, in milliseconds. Set this parameter to a negative value. The callback is invoked after <i>−Timeout</i> milliseconds. For example, if <i>Timeout</i> is −5000, the callback is invoked after 5000 milliseconds.


### -param key [out, optional]

Receives a key that can be used to cancel the timer. To cancel the wait, call <a href="https://msdn.microsoft.com/55d5c6d6-310e-4f73-bbf4-9ac47a3ed295">RtwqCancelWorkItem</a> and pass this key in the <i>Key</i> parameter.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



