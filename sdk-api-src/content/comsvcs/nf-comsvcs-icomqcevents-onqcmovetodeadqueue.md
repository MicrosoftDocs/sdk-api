---
UID: NF:comsvcs.IComQCEvents.OnQCMoveToDeadQueue
title: IComQCEvents::OnQCMoveToDeadQueue (comsvcs.h)
description: Generated when a message is moved to the dead letter queue and cannot be delivered.
helpviewer_keywords: ["IComQCEvents interface [COM+]","OnQCMoveToDeadQueue method","IComQCEvents.OnQCMoveToDeadQueue","IComQCEvents::OnQCMoveToDeadQueue","OnQCMoveToDeadQueue","OnQCMoveToDeadQueue method [COM+]","OnQCMoveToDeadQueue method [COM+]","IComQCEvents interface","_dtc_IComQCEvents_OnQCMoveToDeadQueue","comsvcs/IComQCEvents::OnQCMoveToDeadQueue","cos.icomqcevents_onqcmovetodeadqueue"]
old-location: cos\icomqcevents_onqcmovetodeadqueue.htm
tech.root: cos
ms.assetid: 54117583-4e8d-4ae9-8262-781f5f81636d
ms.date: 12/05/2018
ms.keywords: IComQCEvents interface [COM+],OnQCMoveToDeadQueue method, IComQCEvents.OnQCMoveToDeadQueue, IComQCEvents::OnQCMoveToDeadQueue, OnQCMoveToDeadQueue, OnQCMoveToDeadQueue method [COM+], OnQCMoveToDeadQueue method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCMoveToDeadQueue, comsvcs/IComQCEvents::OnQCMoveToDeadQueue, cos.icomqcevents_onqcmovetodeadqueue
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
 - IComQCEvents::OnQCMoveToDeadQueue
 - comsvcs/IComQCEvents::OnQCMoveToDeadQueue
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
 - IComQCEvents.OnQCMoveToDeadQueue
---

# IComQCEvents::OnQCMoveToDeadQueue


## -description

Generated when a message is moved to the dead letter queue and cannot be delivered.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidMsgId [in]

The unique identifier for the message.

### -param guidWorkFlowId [in]

This parameter is reserved.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomqcevents">IComQCEvents</a>