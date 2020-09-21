---
UID: NF:comsvcs.IComApp2Events.OnAppActivation2
title: IComApp2Events::OnAppActivation2 (comsvcs.h)
description: Generated when the server application process is loaded.
helpviewer_keywords: ["IComApp2Events interface [COM+]","OnAppActivation2 method","IComApp2Events.OnAppActivation2","IComApp2Events::OnAppActivation2","OnAppActivation2","OnAppActivation2 method [COM+]","OnAppActivation2 method [COM+]","IComApp2Events interface","_dtc_IComApp2Events_OnAppActivation2","comsvcs/IComApp2Events::OnAppActivation2","cos.icomapp2events_onappactivation2"]
old-location: cos\icomapp2events_onappactivation2.htm
tech.root: cos
ms.assetid: d621f46e-19c2-4fab-8820-a5716cb7cdc4
ms.date: 12/05/2018
ms.keywords: IComApp2Events interface [COM+],OnAppActivation2 method, IComApp2Events.OnAppActivation2, IComApp2Events::OnAppActivation2, OnAppActivation2, OnAppActivation2 method [COM+], OnAppActivation2 method [COM+],IComApp2Events interface, _dtc_IComApp2Events_OnAppActivation2, comsvcs/IComApp2Events::OnAppActivation2, cos.icomapp2events_onappactivation2
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IComApp2Events::OnAppActivation2
 - comsvcs/IComApp2Events::OnAppActivation2
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
 - IComApp2Events.OnAppActivation2
---

# IComApp2Events::OnAppActivation2


## -description

Generated when the server application process is loaded.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidApp [in]

The GUID of the application.

### -param guidProcess [in]

The process ID.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomapp2events">IComApp2Events</a>