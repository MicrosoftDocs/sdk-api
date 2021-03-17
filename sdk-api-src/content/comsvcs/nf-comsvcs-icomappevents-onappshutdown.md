---
UID: NF:comsvcs.IComAppEvents.OnAppShutdown
title: IComAppEvents::OnAppShutdown (comsvcs.h)
description: Generated when an application server shuts down.
helpviewer_keywords: ["IComAppEvents interface [COM+]","OnAppShutdown method","IComAppEvents.OnAppShutdown","IComAppEvents::OnAppShutdown","OnAppShutdown","OnAppShutdown method [COM+]","OnAppShutdown method [COM+]","IComAppEvents interface","_dtc_IComAppEvents_OnAppShutdown","comsvcs/IComAppEvents::OnAppShutdown","cos.icomappevents_onappshutdown"]
old-location: cos\icomappevents_onappshutdown.htm
tech.root: cos
ms.assetid: d4e35147-48c4-4c77-a648-ffd317aa7861
ms.date: 12/05/2018
ms.keywords: IComAppEvents interface [COM+],OnAppShutdown method, IComAppEvents.OnAppShutdown, IComAppEvents::OnAppShutdown, OnAppShutdown, OnAppShutdown method [COM+], OnAppShutdown method [COM+],IComAppEvents interface, _dtc_IComAppEvents_OnAppShutdown, comsvcs/IComAppEvents::OnAppShutdown, cos.icomappevents_onappshutdown
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
 - IComAppEvents::OnAppShutdown
 - comsvcs/IComAppEvents::OnAppShutdown
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
 - IComAppEvents.OnAppShutdown
---

# IComAppEvents::OnAppShutdown


## -description

Generated when an application server shuts down.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidApp [in]

The globally unique identifier (GUID) of the application.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomappevents">IComAppEvents</a>