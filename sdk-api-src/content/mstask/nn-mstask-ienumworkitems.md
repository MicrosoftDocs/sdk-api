---
UID: NN:mstask.IEnumWorkItems
title: IEnumWorkItems (mstask.h)
description: Provides the methods for enumerating the tasks in the Scheduled Tasks folder.
helpviewer_keywords: ["IEnumWorkItems","IEnumWorkItems interface [Task Scheduler]","IEnumWorkItems interface [Task Scheduler]","described","_msb_ienumworkitems","mstask/IEnumWorkItems","taskschd.ienumworkitems"]
old-location: taskschd\ienumworkitems.htm
tech.root: taskschd
ms.assetid: 1af162e5-8ba1-4d2e-9451-39c80ac0eecf
ms.date: 12/05/2018
ms.keywords: IEnumWorkItems, IEnumWorkItems interface [Task Scheduler], IEnumWorkItems interface [Task Scheduler],described, _msb_ienumworkitems, mstask/IEnumWorkItems, taskschd.ienumworkitems
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
 - IEnumWorkItems
 - mstask/IEnumWorkItems
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
 - IEnumWorkItems
---

# IEnumWorkItems interface


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for enumerating the tasks in the <a href="/windows/desktop/TaskSchd/s">Scheduled Tasks folder</a>.

<b>IEnumWorkItems</b> is the primary interface of the <a href="/windows/desktop/TaskSchd/e">enumeration object</a>. To create the enumeration, call 
<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-enum">ITaskScheduler::Enum</a>.

## -inheritance

The <b>IEnumWorkItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumWorkItems</b> also has these types of members:

