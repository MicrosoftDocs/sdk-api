---
UID: NF:comsvcs.IComQCEvents.OnQCPlayback
title: IComQCEvents::OnQCPlayback (comsvcs.h)
description: Generated when a messages contents are replayed.
helpviewer_keywords: ["IComQCEvents interface [COM+]","OnQCPlayback method","IComQCEvents.OnQCPlayback","IComQCEvents::OnQCPlayback","OnQCPlayback","OnQCPlayback method [COM+]","OnQCPlayback method [COM+]","IComQCEvents interface","_dtc_IComQCEvents_OnQCPlayback","comsvcs/IComQCEvents::OnQCPlayback","cos.icomqcevents_onqcplayback"]
old-location: cos\icomqcevents_onqcplayback.htm
tech.root: cos
ms.assetid: 7cd9daf8-cc4d-4d48-b547-95b370f5a927
ms.date: 12/05/2018
ms.keywords: IComQCEvents interface [COM+],OnQCPlayback method, IComQCEvents.OnQCPlayback, IComQCEvents::OnQCPlayback, OnQCPlayback, OnQCPlayback method [COM+], OnQCPlayback method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCPlayback, comsvcs/IComQCEvents::OnQCPlayback, cos.icomqcevents_onqcplayback
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
 - IComQCEvents::OnQCPlayback
 - comsvcs/IComQCEvents::OnQCPlayback
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
 - IComQCEvents.OnQCPlayback
---

# IComQCEvents::OnQCPlayback


## -description

Generated when a messages contents are replayed.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param objid [in]

The just-in-time activated object.

### -param guidMsgId [in]

The unique identifier for the queue.

### -param guidWorkFlowId [in]

This parameter is reserved.

### -param hr [in]

The status from Message Queuing receive message.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomqcevents">IComQCEvents</a>