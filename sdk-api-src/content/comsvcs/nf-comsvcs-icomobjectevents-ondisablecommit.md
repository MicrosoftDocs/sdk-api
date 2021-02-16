---
UID: NF:comsvcs.IComObjectEvents.OnDisableCommit
title: IComObjectEvents::OnDisableCommit (comsvcs.h)
description: Generated when the client calls DisableCommit on a context.
helpviewer_keywords: ["IComObjectEvents interface [COM+]","OnDisableCommit method","IComObjectEvents.OnDisableCommit","IComObjectEvents::OnDisableCommit","OnDisableCommit","OnDisableCommit method [COM+]","OnDisableCommit method [COM+]","IComObjectEvents interface","_dtc_IComObjectEvents_OnDisableCommit","comsvcs/IComObjectEvents::OnDisableCommit","cos.icomobjectevents_ondisablecommit"]
old-location: cos\icomobjectevents_ondisablecommit.htm
tech.root: cos
ms.assetid: 413d7216-294c-4e46-b24c-abe1d1a09239
ms.date: 12/05/2018
ms.keywords: IComObjectEvents interface [COM+],OnDisableCommit method, IComObjectEvents.OnDisableCommit, IComObjectEvents::OnDisableCommit, OnDisableCommit, OnDisableCommit method [COM+], OnDisableCommit method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnDisableCommit, comsvcs/IComObjectEvents::OnDisableCommit, cos.icomobjectevents_ondisablecommit
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
 - IComObjectEvents::OnDisableCommit
 - comsvcs/IComObjectEvents::OnDisableCommit
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
 - IComObjectEvents.OnDisableCommit
---

# IComObjectEvents::OnDisableCommit


## -description

Generated when the client calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-disablecommit">DisableCommit</a> on a context.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param CtxtID [in]

The GUID of the current context.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectevents">IComObjectEvents</a>