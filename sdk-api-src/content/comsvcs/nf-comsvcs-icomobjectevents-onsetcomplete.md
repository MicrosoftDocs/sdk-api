---
UID: NF:comsvcs.IComObjectEvents.OnSetComplete
title: IComObjectEvents::OnSetComplete (comsvcs.h)
description: Generated when the client calls SetComplete on a context.
helpviewer_keywords: ["IComObjectEvents interface [COM+]","OnSetComplete method","IComObjectEvents.OnSetComplete","IComObjectEvents::OnSetComplete","OnSetComplete","OnSetComplete method [COM+]","OnSetComplete method [COM+]","IComObjectEvents interface","_dtc_IComObjectEvents_OnSetComplete","comsvcs/IComObjectEvents::OnSetComplete","cos.icomobjectevents_onsetcomplete"]
old-location: cos\icomobjectevents_onsetcomplete.htm
tech.root: cos
ms.assetid: 3bda05b7-3306-428c-b920-d87eee0b35d7
ms.date: 12/05/2018
ms.keywords: IComObjectEvents interface [COM+],OnSetComplete method, IComObjectEvents.OnSetComplete, IComObjectEvents::OnSetComplete, OnSetComplete, OnSetComplete method [COM+], OnSetComplete method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnSetComplete, comsvcs/IComObjectEvents::OnSetComplete, cos.icomobjectevents_onsetcomplete
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
 - IComObjectEvents::OnSetComplete
 - comsvcs/IComObjectEvents::OnSetComplete
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
 - IComObjectEvents.OnSetComplete
---

# IComObjectEvents::OnSetComplete


## -description

Generated when the client calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> on a context.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param CtxtID [in]

The GUID of the current context.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectevents">IComObjectEvents</a>