---
UID: NF:comsvcs.IComObjectEvents.OnEnableCommit
title: IComObjectEvents::OnEnableCommit (comsvcs.h)
description: Generated when the client calls EnableCommit on a context.
helpviewer_keywords: ["IComObjectEvents interface [COM+]","OnEnableCommit method","IComObjectEvents.OnEnableCommit","IComObjectEvents::OnEnableCommit","OnEnableCommit","OnEnableCommit method [COM+]","OnEnableCommit method [COM+]","IComObjectEvents interface","_dtc_IComObjectEvents_OnEnableCommit","comsvcs/IComObjectEvents::OnEnableCommit","cos.icomobjectevents_onenablecommit"]
old-location: cos\icomobjectevents_onenablecommit.htm
tech.root: cos
ms.assetid: 88fdf857-1dbd-4a6b-87c6-0d72eeeab9b4
ms.date: 12/05/2018
ms.keywords: IComObjectEvents interface [COM+],OnEnableCommit method, IComObjectEvents.OnEnableCommit, IComObjectEvents::OnEnableCommit, OnEnableCommit, OnEnableCommit method [COM+], OnEnableCommit method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnEnableCommit, comsvcs/IComObjectEvents::OnEnableCommit, cos.icomobjectevents_onenablecommit
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
 - IComObjectEvents::OnEnableCommit
 - comsvcs/IComObjectEvents::OnEnableCommit
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
 - IComObjectEvents.OnEnableCommit
---

# IComObjectEvents::OnEnableCommit


## -description

Generated when the client calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-enablecommit">EnableCommit</a> on a context.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param CtxtID [in]

The GUID of the current context.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectevents">IComObjectEvents</a>