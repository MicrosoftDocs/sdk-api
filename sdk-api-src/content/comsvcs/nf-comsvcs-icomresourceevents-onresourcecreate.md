---
UID: NF:comsvcs.IComResourceEvents.OnResourceCreate
title: IComResourceEvents::OnResourceCreate (comsvcs.h)
description: Generated when a new resource is created and allocated.
helpviewer_keywords: ["IComResourceEvents interface [COM+]","OnResourceCreate method","IComResourceEvents.OnResourceCreate","IComResourceEvents::OnResourceCreate","OnResourceCreate","OnResourceCreate method [COM+]","OnResourceCreate method [COM+]","IComResourceEvents interface","_dtc_IComResourceEvents_OnResourceCreate","comsvcs/IComResourceEvents::OnResourceCreate","cos.icomresourceevents_onresourcecreate"]
old-location: cos\icomresourceevents_onresourcecreate.htm
tech.root: cos
ms.assetid: 6c1cb030-c6c7-4f91-a1ea-eebbec41813b
ms.date: 12/05/2018
ms.keywords: IComResourceEvents interface [COM+],OnResourceCreate method, IComResourceEvents.OnResourceCreate, IComResourceEvents::OnResourceCreate, OnResourceCreate, OnResourceCreate method [COM+], OnResourceCreate method [COM+],IComResourceEvents interface, _dtc_IComResourceEvents_OnResourceCreate, comsvcs/IComResourceEvents::OnResourceCreate, cos.icomresourceevents_onresourcecreate
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
 - IComResourceEvents::OnResourceCreate
 - comsvcs/IComResourceEvents::OnResourceCreate
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
 - IComResourceEvents.OnResourceCreate
---

# IComResourceEvents::OnResourceCreate


## -description

Generated when a new resource is created and allocated.

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