---
UID: NF:comsvcs.IComResourceEvents.OnResourceAllocate
title: IComResourceEvents::OnResourceAllocate (comsvcs.h)
description: Generated when an existing resource is allocated.
helpviewer_keywords: ["IComResourceEvents interface [COM+]","OnResourceAllocate method","IComResourceEvents.OnResourceAllocate","IComResourceEvents::OnResourceAllocate","OnResourceAllocate","OnResourceAllocate method [COM+]","OnResourceAllocate method [COM+]","IComResourceEvents interface","_dtc_IComResourceEvents_OnResourceAllocate","comsvcs/IComResourceEvents::OnResourceAllocate","cos.icomresourceevents_onresourceallocate"]
old-location: cos\icomresourceevents_onresourceallocate.htm
tech.root: cos
ms.assetid: f063230d-a0b8-46c5-845c-f94aefb706a7
ms.date: 12/05/2018
ms.keywords: IComResourceEvents interface [COM+],OnResourceAllocate method, IComResourceEvents.OnResourceAllocate, IComResourceEvents::OnResourceAllocate, OnResourceAllocate, OnResourceAllocate method [COM+], OnResourceAllocate method [COM+],IComResourceEvents interface, _dtc_IComResourceEvents_OnResourceAllocate, comsvcs/IComResourceEvents::OnResourceAllocate, cos.icomresourceevents_onresourceallocate
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
 - IComResourceEvents::OnResourceAllocate
 - comsvcs/IComResourceEvents::OnResourceAllocate
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
 - IComResourceEvents.OnResourceAllocate
---

# IComResourceEvents::OnResourceAllocate


## -description

Generated when an existing resource is allocated.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param ObjectID [in]

The just-in-time activated object.

### -param pszType [in]

A description of the resource.

### -param resId [in]

The unique identifier for the resource.

### -param enlisted [in]

Indicates whether the resource is enlisted in a transaction.

### -param NumRated [in]

The number of possible resources evaluated for a match.

### -param Rating [in]

The rating of the resource actually selected.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomresourceevents">IComResourceEvents</a>