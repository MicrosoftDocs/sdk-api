---
UID: NF:comsvcs.IComObjectEvents.OnObjectDeactivate
title: IComObjectEvents::OnObjectDeactivate (comsvcs.h)
author: windows-sdk-content
description: Generated when the JIT-activated object is freed by SetComplete or SetAbort.
old-location: cos\icomobjectevents_onobjectdeactivate.htm
tech.root: cossdk
ms.assetid: 3284da44-bcc4-49eb-9aa8-40061bf51869
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComObjectEvents interface [COM+],OnObjectDeactivate method, IComObjectEvents.OnObjectDeactivate, IComObjectEvents::OnObjectDeactivate, OnObjectDeactivate, OnObjectDeactivate method [COM+], OnObjectDeactivate method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnObjectDeactivate, comsvcs/IComObjectEvents::OnObjectDeactivate, cos.icomobjectevents_onobjectdeactivate
ms.topic: method
f1_keywords: 
 - "comsvcs/IComObjectEvents.OnObjectDeactivate"
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
 - IComObjectEvents.OnObjectDeactivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComObjectEvents::OnObjectDeactivate


## -description


Generated when the JIT-activated object is freed by <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a>.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.


### -param CtxtID [in]

The GUID of the current context.


### -param ObjectID [in]

The JIT-activated object.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectevents">IComObjectEvents</a>
 

 

