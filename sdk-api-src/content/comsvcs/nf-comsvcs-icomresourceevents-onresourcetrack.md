---
UID: NF:comsvcs.IComResourceEvents.OnResourceTrack
title: IComResourceEvents::OnResourceTrack (comsvcs.h)
description: Generated when a resource is tracked.
helpviewer_keywords: ["IComResourceEvents interface [COM+]","OnResourceTrack method","IComResourceEvents.OnResourceTrack","IComResourceEvents::OnResourceTrack","OnResourceTrack","OnResourceTrack method [COM+]","OnResourceTrack method [COM+]","IComResourceEvents interface","_dtc_IComResourceEvents_OnResourceTrack","comsvcs/IComResourceEvents::OnResourceTrack","cos.icomresourceevents_onresourcetrack"]
old-location: cos\icomresourceevents_onresourcetrack.htm
tech.root: cos
ms.assetid: 8845cf07-f796-45bd-9d3d-261cf0903050
ms.date: 12/05/2018
ms.keywords: IComResourceEvents interface [COM+],OnResourceTrack method, IComResourceEvents.OnResourceTrack, IComResourceEvents::OnResourceTrack, OnResourceTrack, OnResourceTrack method [COM+], OnResourceTrack method [COM+],IComResourceEvents interface, _dtc_IComResourceEvents_OnResourceTrack, comsvcs/IComResourceEvents::OnResourceTrack, cos.icomresourceevents_onresourcetrack
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
 - IComResourceEvents::OnResourceTrack
 - comsvcs/IComResourceEvents::OnResourceTrack
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
 - IComResourceEvents.OnResourceTrack
---

# IComResourceEvents::OnResourceTrack


## -description

Generated when a resource is tracked.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param ObjectID [in]

The just-in-time activated object.

### -param pszType [in]

A description of the resource.

### -param resId [in]

The unique identifier of the resource.

### -param enlisted [in]

Indicates whether the resource is enlisted in a transaction.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomresourceevents">IComResourceEvents</a>