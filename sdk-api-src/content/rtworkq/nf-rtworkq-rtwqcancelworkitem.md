---
UID: NF:rtworkq.RtwqCancelWorkItem
title: RtwqCancelWorkItem function
author: windows-driver-content
description: Attempts to cancel an asynchronous operation that was scheduled with RtwqScheduleWorkItem.
old-location: base\rtwqcancelworkitem.htm
old-project: ProcThread
ms.assetid: 55d5c6d6-310e-4f73-bbf4-9ac47a3ed295
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: RtwqCancelWorkItem, RtwqCancelWorkItem function, base.rtwqcancelworkitem, rtworkq/RtwqCancelWorkItem
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
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RTWorkQ.dll
api_name:
-	RtwqCancelWorkItem
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtwqCancelWorkItem function


## -description



          Attempts to cancel an asynchronous operation that was scheduled with <a href="https://msdn.microsoft.com/cfc22cfb-44fc-441b-826c-61f72cb0bd68">RtwqScheduleWorkItem</a>.


## -parameters




### -param Key [in]


            The key that was received in the <i>key</i> parameter of the <a href="https://msdn.microsoft.com/cfc22cfb-44fc-441b-826c-61f72cb0bd68">RtwqScheduleWorkItem</a>.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Because work items are asynchronous, the  work-item callback might still be invoked after <b>RtwqCancelWorkItem</b> is called.



