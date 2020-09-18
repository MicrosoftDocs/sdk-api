---
UID: NF:comsvcs.IComQCEvents.OnQCQueueOpen
title: IComQCEvents::OnQCQueueOpen (comsvcs.h)
description: Generated when a queued components queue is opened.
helpviewer_keywords: ["IComQCEvents interface [COM+]","OnQCQueueOpen method","IComQCEvents.OnQCQueueOpen","IComQCEvents::OnQCQueueOpen","OnQCQueueOpen","OnQCQueueOpen method [COM+]","OnQCQueueOpen method [COM+]","IComQCEvents interface","_dtc_IComQCEvents_OnQCQueueOpen","comsvcs/IComQCEvents::OnQCQueueOpen","cos.icomqcevents_onqcqueueopen"]
old-location: cos\icomqcevents_onqcqueueopen.htm
tech.root: cos
ms.assetid: 7dcd1726-650a-4bb5-ae12-48c6989e1692
ms.date: 12/05/2018
ms.keywords: IComQCEvents interface [COM+],OnQCQueueOpen method, IComQCEvents.OnQCQueueOpen, IComQCEvents::OnQCQueueOpen, OnQCQueueOpen, OnQCQueueOpen method [COM+], OnQCQueueOpen method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCQueueOpen, comsvcs/IComQCEvents::OnQCQueueOpen, cos.icomqcevents_onqcqueueopen
req.header: comsvcs.h
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
 - IComQCEvents::OnQCQueueOpen
 - comsvcs/IComQCEvents::OnQCQueueOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComQCEvents.OnQCQueueOpen
---

# IComQCEvents::OnQCQueueOpen


## -description

Generated when a queued components queue is opened. This method is used to generate the <i>QueueID</i> parameter.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param szQueue [in]

The name of the queue.

### -param QueueID [in]

The unique identifier for the queue.

### -param hr [in]

The status from Message Queuing queue open.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomqcevents">IComQCEvents</a>