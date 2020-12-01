---
UID: NF:comsvcs.IComThreadEvents.OnThreadTerminate
title: IComThreadEvents::OnThreadTerminate (comsvcs.h)
description: Generated when a single-threaded apartment (STA) thread is terminated.
helpviewer_keywords: ["IComThreadEvents interface [COM+]","OnThreadTerminate method","IComThreadEvents.OnThreadTerminate","IComThreadEvents::OnThreadTerminate","OnThreadTerminate","OnThreadTerminate method [COM+]","OnThreadTerminate method [COM+]","IComThreadEvents interface","_dtc_IComThreadEvents_OnThreadTerminate","comsvcs/IComThreadEvents::OnThreadTerminate","cos.icomthreadevents_onthreadterminate"]
old-location: cos\icomthreadevents_onthreadterminate.htm
tech.root: cos
ms.assetid: 8483962c-46c9-4ef1-8c7e-391a04334293
ms.date: 12/05/2018
ms.keywords: IComThreadEvents interface [COM+],OnThreadTerminate method, IComThreadEvents.OnThreadTerminate, IComThreadEvents::OnThreadTerminate, OnThreadTerminate, OnThreadTerminate method [COM+], OnThreadTerminate method [COM+],IComThreadEvents interface, _dtc_IComThreadEvents_OnThreadTerminate, comsvcs/IComThreadEvents::OnThreadTerminate, cos.icomthreadevents_onthreadterminate
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
 - IComThreadEvents::OnThreadTerminate
 - comsvcs/IComThreadEvents::OnThreadTerminate
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
 - IComThreadEvents.OnThreadTerminate
---

# IComThreadEvents::OnThreadTerminate


## -description

Generated when a single-threaded apartment (STA) thread is terminated.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param ThreadID [in]

The unique thread identifier.

### -param dwThread [in]

The Windows thread identifier.

### -param dwTheadCnt [in]

The number of threads in the STA thread pool.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomthreadevents">IComThreadEvents</a>