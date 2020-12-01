---
UID: NF:comsvcs.IManagedObjectInfo.GetIUnknown
title: IManagedObjectInfo::GetIUnknown (comsvcs.h)
description: Retrieves the IUnknown interface that is associated with the managed object.
helpviewer_keywords: ["GetIUnknown","GetIUnknown method [COM+]","GetIUnknown method [COM+]","IManagedObjectInfo interface","IManagedObjectInfo interface [COM+]","GetIUnknown method","IManagedObjectInfo.GetIUnknown","IManagedObjectInfo::GetIUnknown","_cos_IManagedObjectInfo_GetIUnknown","comsvcs/IManagedObjectInfo::GetIUnknown","cos.imanagedobjectinfo_getiunknown"]
old-location: cos\imanagedobjectinfo_getiunknown.htm
tech.root: cos
ms.assetid: 1c0d27cb-1725-4654-ab15-0ef815ce6657
ms.date: 12/05/2018
ms.keywords: GetIUnknown, GetIUnknown method [COM+], GetIUnknown method [COM+],IManagedObjectInfo interface, IManagedObjectInfo interface [COM+],GetIUnknown method, IManagedObjectInfo.GetIUnknown, IManagedObjectInfo::GetIUnknown, _cos_IManagedObjectInfo_GetIUnknown, comsvcs/IManagedObjectInfo::GetIUnknown, cos.imanagedobjectinfo_getiunknown
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IManagedObjectInfo::GetIUnknown
 - comsvcs/IManagedObjectInfo::GetIUnknown
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
 - IManagedObjectInfo.GetIUnknown
---

# IManagedObjectInfo::GetIUnknown


## -description

Retrieves the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface that is associated with the managed object.

## -parameters

### -param pUnk [out]

A reference to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedobjectinfo">IManagedObjectInfo</a>