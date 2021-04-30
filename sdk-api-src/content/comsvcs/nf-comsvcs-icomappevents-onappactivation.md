---
UID: NF:comsvcs.IComAppEvents.OnAppActivation
title: IComAppEvents::OnAppActivation (comsvcs.h)
description: Generated when an application server starts.
helpviewer_keywords: ["IComAppEvents interface [COM+]","OnAppActivation method","IComAppEvents.OnAppActivation","IComAppEvents::OnAppActivation","OnAppActivation","OnAppActivation method [COM+]","OnAppActivation method [COM+]","IComAppEvents interface","_dtc_IComAppEvents_OnAppActivation","comsvcs/IComAppEvents::OnAppActivation","cos.icomappevents_onappactivation"]
old-location: cos\icomappevents_onappactivation.htm
tech.root: cos
ms.assetid: 4561d15a-6c1b-48e7-9697-87dfb51f877c
ms.date: 12/05/2018
ms.keywords: IComAppEvents interface [COM+],OnAppActivation method, IComAppEvents.OnAppActivation, IComAppEvents::OnAppActivation, OnAppActivation, OnAppActivation method [COM+], OnAppActivation method [COM+],IComAppEvents interface, _dtc_IComAppEvents_OnAppActivation, comsvcs/IComAppEvents::OnAppActivation, cos.icomappevents_onappactivation
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
 - IComAppEvents::OnAppActivation
 - comsvcs/IComAppEvents::OnAppActivation
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
 - IComAppEvents.OnAppActivation
---

# IComAppEvents::OnAppActivation


## -description

Generated when an application server starts.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidApp [in]

The globally unique identifier (GUID) of the application.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomappevents">IComAppEvents</a>