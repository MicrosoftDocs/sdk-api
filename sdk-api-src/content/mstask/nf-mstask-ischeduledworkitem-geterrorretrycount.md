---
UID: NF:mstask.IScheduledWorkItem.GetErrorRetryCount
title: IScheduledWorkItem::GetErrorRetryCount (mstask.h)
description: Retrieves the number of times that the Task Scheduler will retry an operation when an error occurs. This method is not implemented.
helpviewer_keywords: ["GetErrorRetryCount","GetErrorRetryCount method [Task Scheduler]","GetErrorRetryCount method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetErrorRetryCount method","IScheduledWorkItem.GetErrorRetryCount","IScheduledWorkItem::GetErrorRetryCount","_msb_ischeduledworkitem_geterrorretrycount","mstask/IScheduledWorkItem::GetErrorRetryCount","taskschd.ischeduledworkitem_geterrorretrycount"]
old-location: taskschd\ischeduledworkitem_geterrorretrycount.htm
tech.root: taskschd
ms.assetid: f9935325-124b-4c21-be9c-e9d48fb69791
ms.date: 12/05/2018
ms.keywords: GetErrorRetryCount, GetErrorRetryCount method [Task Scheduler], GetErrorRetryCount method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetErrorRetryCount method, IScheduledWorkItem.GetErrorRetryCount, IScheduledWorkItem::GetErrorRetryCount, _msb_ischeduledworkitem_geterrorretrycount, mstask/IScheduledWorkItem::GetErrorRetryCount, taskschd.ischeduledworkitem_geterrorretrycount
req.header: mstask.h
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
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - IScheduledWorkItem::GetErrorRetryCount
 - mstask/IScheduledWorkItem::GetErrorRetryCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem.GetErrorRetryCount
---

# IScheduledWorkItem::GetErrorRetryCount


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the number of times that the Task Scheduler will retry an operation when an error occurs. This method is not implemented.

## -parameters

### -param pwRetryCount [out]

A pointer to a <b>WORD</b> that contains the number of times to retry.

## -returns

Not implemented.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-seterrorretrycount">SetErrorRetryCount</a>