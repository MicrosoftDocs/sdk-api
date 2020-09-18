---
UID: NF:comsvcs.IComQCEvents.OnQCMoveToReTryQueue
title: IComQCEvents::OnQCMoveToReTryQueue (comsvcs.h)
description: Generated when a message is moved to a queued components retry queue.
helpviewer_keywords: ["IComQCEvents interface [COM+]","OnQCMoveToReTryQueue method","IComQCEvents.OnQCMoveToReTryQueue","IComQCEvents::OnQCMoveToReTryQueue","OnQCMoveToReTryQueue","OnQCMoveToReTryQueue method [COM+]","OnQCMoveToReTryQueue method [COM+]","IComQCEvents interface","_dtc_IComQCEvents_OnQCMoveToReTryQueue","comsvcs/IComQCEvents::OnQCMoveToReTryQueue","cos.icomqcevents_onqcmovetoretryqueue"]
old-location: cos\icomqcevents_onqcmovetoretryqueue.htm
tech.root: cos
ms.assetid: d8f2af02-852d-4e36-9e0c-4919e2fba4a1
ms.date: 12/05/2018
ms.keywords: IComQCEvents interface [COM+],OnQCMoveToReTryQueue method, IComQCEvents.OnQCMoveToReTryQueue, IComQCEvents::OnQCMoveToReTryQueue, OnQCMoveToReTryQueue, OnQCMoveToReTryQueue method [COM+], OnQCMoveToReTryQueue method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCMoveToReTryQueue, comsvcs/IComQCEvents::OnQCMoveToReTryQueue, cos.icomqcevents_onqcmovetoretryqueue
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
 - IComQCEvents::OnQCMoveToReTryQueue
 - comsvcs/IComQCEvents::OnQCMoveToReTryQueue
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
 - IComQCEvents.OnQCMoveToReTryQueue
---

# IComQCEvents::OnQCMoveToReTryQueue


## -description

Generated when a message is moved to a queued components retry queue.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidMsgId [in]

The unique identifier for the message.

### -param guidWorkFlowId [in]

This parameter is reserved.

### -param RetryIndex [in]

The index number of the retry queue where the message moved.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomqcevents">IComQCEvents</a>