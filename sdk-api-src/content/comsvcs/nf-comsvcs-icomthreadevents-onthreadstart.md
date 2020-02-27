---
UID: NF:comsvcs.IComThreadEvents.OnThreadStart
title: IComThreadEvents::OnThreadStart (comsvcs.h)
description: Generated when a single-threaded apartment (STA) thread is started.
old-location: cos\icomthreadevents_onthreadstart.htm
tech.root: cossdk
ms.assetid: 9316965e-13e8-4e3a-9404-8e49334773bc
ms.date: 12/05/2018
ms.keywords: IComThreadEvents interface [COM+],OnThreadStart method, IComThreadEvents.OnThreadStart, IComThreadEvents::OnThreadStart, OnThreadStart, OnThreadStart method [COM+], OnThreadStart method [COM+],IComThreadEvents interface, _dtc_IComThreadEvents_OnThreadStart, comsvcs/IComThreadEvents::OnThreadStart, cos.icomthreadevents_onthreadstart
f1_keywords:
- comsvcs/IComThreadEvents.OnThreadStart
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IComThreadEvents.OnThreadStart
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComThreadEvents::OnThreadStart


## -description


Generated when a single-threaded apartment (STA) thread is started.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.


### -param ThreadID [in]

The unique thread identifier.


### -param dwThread [in]

The Windows thread identifier.


### -param dwTheadCnt [in]

The number of threads in the STA thread pool.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomthreadevents">IComThreadEvents</a>
 

 

