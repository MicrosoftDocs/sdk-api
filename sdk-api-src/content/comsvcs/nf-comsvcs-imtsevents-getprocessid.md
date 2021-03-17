---
UID: NF:comsvcs.IMtsEvents.GetProcessID
title: IMtsEvents::GetProcessID (comsvcs.h)
description: Retrieves the identifier of the process in which the event occurred.
helpviewer_keywords: ["GetProcessID","GetProcessID method [COM+]","GetProcessID method [COM+]","IMtsEvents interface","IMtsEvents interface [COM+]","GetProcessID method","IMtsEvents.GetProcessID","IMtsEvents::GetProcessID","_dtc_IMtsEvents_GetProcessID","comsvcs/IMtsEvents::GetProcessID","cos.imtsevents_getprocessid"]
old-location: cos\imtsevents_getprocessid.htm
tech.root: cos
ms.assetid: 9950eeab-0b90-4810-9163-8c5582d0b748
ms.date: 12/05/2018
ms.keywords: GetProcessID, GetProcessID method [COM+], GetProcessID method [COM+],IMtsEvents interface, IMtsEvents interface [COM+],GetProcessID method, IMtsEvents.GetProcessID, IMtsEvents::GetProcessID, _dtc_IMtsEvents_GetProcessID, comsvcs/IMtsEvents::GetProcessID, cos.imtsevents_getprocessid
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
 - IMtsEvents::GetProcessID
 - comsvcs/IMtsEvents::GetProcessID
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
 - IMtsEvents.GetProcessID
---

# IMtsEvents::GetProcessID


## -description

Retrieves the identifier of the process in which the event occurred.

## -parameters

### -param id [out]

A pointer to the process identification for the event.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsevents">IMtsEvents</a>