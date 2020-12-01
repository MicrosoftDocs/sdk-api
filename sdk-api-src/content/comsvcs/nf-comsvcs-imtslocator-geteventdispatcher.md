---
UID: NF:comsvcs.IMTSLocator.GetEventDispatcher
title: IMTSLocator::GetEventDispatcher (comsvcs.h)
description: Retrieves a pointer to the event dispatcher for the current process.
helpviewer_keywords: ["GetEventDispatcher","GetEventDispatcher method [COM+]","GetEventDispatcher method [COM+]","IMTSLocator interface","IMTSLocator interface [COM+]","GetEventDispatcher method","IMTSLocator.GetEventDispatcher","IMTSLocator::GetEventDispatcher","_dtc_IMtsLocator_GetEventDispatcher","comsvcs/IMTSLocator::GetEventDispatcher","cos.imtslocator_geteventdispatcher"]
old-location: cos\imtslocator_geteventdispatcher.htm
tech.root: cos
ms.assetid: 10e110bf-1a7c-48a2-ab9f-836ea21d442b
ms.date: 12/05/2018
ms.keywords: GetEventDispatcher, GetEventDispatcher method [COM+], GetEventDispatcher method [COM+],IMTSLocator interface, IMTSLocator interface [COM+],GetEventDispatcher method, IMTSLocator.GetEventDispatcher, IMTSLocator::GetEventDispatcher, _dtc_IMtsLocator_GetEventDispatcher, comsvcs/IMTSLocator::GetEventDispatcher, cos.imtslocator_geteventdispatcher
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
 - IMTSLocator::GetEventDispatcher
 - comsvcs/IMTSLocator::GetEventDispatcher
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
 - IMTSLocator.GetEventDispatcher
---

# IMTSLocator::GetEventDispatcher


## -description

Retrieves a pointer to the event dispatcher for the current process.

## -parameters

### -param pUnk [out]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the event dispatcher for the current process.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtslocator">IMTSLocator</a>