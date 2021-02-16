---
UID: NF:comsvcs.IComApp2Events.OnAppForceShutdown2
title: IComApp2Events::OnAppForceShutdown2 (comsvcs.h)
description: Generated when the server application is forced to shut down.
helpviewer_keywords: ["IComApp2Events interface [COM+]","OnAppForceShutdown2 method","IComApp2Events.OnAppForceShutdown2","IComApp2Events::OnAppForceShutdown2","OnAppForceShutdown2","OnAppForceShutdown2 method [COM+]","OnAppForceShutdown2 method [COM+]","IComApp2Events interface","_dtc_IComApp2Events_OnAppForceShutdown2","comsvcs/IComApp2Events::OnAppForceShutdown2","cos.icomapp2events_onappforceshutdown2"]
old-location: cos\icomapp2events_onappforceshutdown2.htm
tech.root: cos
ms.assetid: 7658caaa-a995-4b88-a314-b5cd981d1ec6
ms.date: 12/05/2018
ms.keywords: IComApp2Events interface [COM+],OnAppForceShutdown2 method, IComApp2Events.OnAppForceShutdown2, IComApp2Events::OnAppForceShutdown2, OnAppForceShutdown2, OnAppForceShutdown2 method [COM+], OnAppForceShutdown2 method [COM+],IComApp2Events interface, _dtc_IComApp2Events_OnAppForceShutdown2, comsvcs/IComApp2Events::OnAppForceShutdown2, cos.icomapp2events_onappforceshutdown2
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
 - IComApp2Events::OnAppForceShutdown2
 - comsvcs/IComApp2Events::OnAppForceShutdown2
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
 - IComApp2Events.OnAppForceShutdown2
---

# IComApp2Events::OnAppForceShutdown2


## -description

Generated when the server application is forced to shut down.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidApp [in]

The GUID of the application.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomapp2events">IComApp2Events</a>