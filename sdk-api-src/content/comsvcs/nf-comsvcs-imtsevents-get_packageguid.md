---
UID: NF:comsvcs.IMtsEvents.get_PackageGuid
title: IMtsEvents::get_PackageGuid (comsvcs.h)
description: Retrieves the globally unique identifier (GUID) for the package in which the event occurred.
helpviewer_keywords: ["IMtsEvents interface [COM+]","get_PackageGuid method","IMtsEvents.get_PackageGuid","IMtsEvents::get_PackageGuid","_dtc_IMtsEvents_PackageGuid","comsvcs/IMtsEvents::get_PackageGuid","cos.imtsevents_get_packageguid","get_PackageGuid","get_PackageGuid method [COM+]","get_PackageGuid method [COM+]","IMtsEvents interface"]
old-location: cos\imtsevents_get_packageguid.htm
tech.root: cos
ms.assetid: 7afd68f7-8aba-4c0f-a262-9a0ea861e063
ms.date: 12/05/2018
ms.keywords: IMtsEvents interface [COM+],get_PackageGuid method, IMtsEvents.get_PackageGuid, IMtsEvents::get_PackageGuid, _dtc_IMtsEvents_PackageGuid, comsvcs/IMtsEvents::get_PackageGuid, cos.imtsevents_get_packageguid, get_PackageGuid, get_PackageGuid method [COM+], get_PackageGuid method [COM+],IMtsEvents interface
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
 - IMtsEvents::get_PackageGuid
 - comsvcs/IMtsEvents::get_PackageGuid
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
 - IMtsEvents.get_PackageGuid
---

# IMtsEvents::get_PackageGuid


## -description

Retrieves the globally unique identifier (GUID) for the package in which the event occurred.

## -parameters

### -param pVal [out]

A pointer to the package GUID.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsevents">IMtsEvents</a>