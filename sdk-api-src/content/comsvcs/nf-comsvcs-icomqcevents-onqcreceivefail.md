---
UID: NF:comsvcs.IComQCEvents.OnQCReceiveFail
title: IComQCEvents::OnQCReceiveFail (comsvcs.h)
description: Generated when the receive message fails.
helpviewer_keywords: ["IComQCEvents interface [COM+]","OnQCReceiveFail method","IComQCEvents.OnQCReceiveFail","IComQCEvents::OnQCReceiveFail","OnQCReceiveFail","OnQCReceiveFail method [COM+]","OnQCReceiveFail method [COM+]","IComQCEvents interface","_dtc_IComQCEvents_OnQCReceiveFail","comsvcs/IComQCEvents::OnQCReceiveFail","cos.icomqcevents_onqcreceivefail"]
old-location: cos\icomqcevents_onqcreceivefail.htm
tech.root: cos
ms.assetid: 21d685ce-b65f-4d13-b653-e6c6d1afa704
ms.date: 12/05/2018
ms.keywords: IComQCEvents interface [COM+],OnQCReceiveFail method, IComQCEvents.OnQCReceiveFail, IComQCEvents::OnQCReceiveFail, OnQCReceiveFail, OnQCReceiveFail method [COM+], OnQCReceiveFail method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCReceiveFail, comsvcs/IComQCEvents::OnQCReceiveFail, cos.icomqcevents_onqcreceivefail
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
 - IComQCEvents::OnQCReceiveFail
 - comsvcs/IComQCEvents::OnQCReceiveFail
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
 - IComQCEvents.OnQCReceiveFail
---

# IComQCEvents::OnQCReceiveFail


## -description

Generated when the receive message fails.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param QueueID [in]

The unique identifier for the queue.

### -param msmqhr [in]

The status from Queued Components processing of the received message.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomqcevents">IComQCEvents</a>