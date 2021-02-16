---
UID: NF:comsvcs.IComObjectEvents.OnObjectDeactivate
title: IComObjectEvents::OnObjectDeactivate (comsvcs.h)
description: Generated when the JIT-activated object is freed by SetComplete or SetAbort.
helpviewer_keywords: ["IComObjectEvents interface [COM+]","OnObjectDeactivate method","IComObjectEvents.OnObjectDeactivate","IComObjectEvents::OnObjectDeactivate","OnObjectDeactivate","OnObjectDeactivate method [COM+]","OnObjectDeactivate method [COM+]","IComObjectEvents interface","_dtc_IComObjectEvents_OnObjectDeactivate","comsvcs/IComObjectEvents::OnObjectDeactivate","cos.icomobjectevents_onobjectdeactivate"]
old-location: cos\icomobjectevents_onobjectdeactivate.htm
tech.root: cos
ms.assetid: 3284da44-bcc4-49eb-9aa8-40061bf51869
ms.date: 12/05/2018
ms.keywords: IComObjectEvents interface [COM+],OnObjectDeactivate method, IComObjectEvents.OnObjectDeactivate, IComObjectEvents::OnObjectDeactivate, OnObjectDeactivate, OnObjectDeactivate method [COM+], OnObjectDeactivate method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnObjectDeactivate, comsvcs/IComObjectEvents::OnObjectDeactivate, cos.icomobjectevents_onobjectdeactivate
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
 - IComObjectEvents::OnObjectDeactivate
 - comsvcs/IComObjectEvents::OnObjectDeactivate
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
 - IComObjectEvents.OnObjectDeactivate
---

# IComObjectEvents::OnObjectDeactivate


## -description

Generated when the JIT-activated object is freed by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a>.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param CtxtID [in]

The GUID of the current context.

### -param ObjectID [in]

The JIT-activated object.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectevents">IComObjectEvents</a>