---
UID: NF:comsvcs.IManagedObjectInfo.GetIObjectControl
title: IManagedObjectInfo::GetIObjectControl (comsvcs.h)
description: Retrieves the IObjectControl interface that is associated with the managed object.
helpviewer_keywords: ["GetIObjectControl","GetIObjectControl method [COM+]","GetIObjectControl method [COM+]","IManagedObjectInfo interface","IManagedObjectInfo interface [COM+]","GetIObjectControl method","IManagedObjectInfo.GetIObjectControl","IManagedObjectInfo::GetIObjectControl","_cos_IManagedObjectInfo_GetIObjectControl","comsvcs/IManagedObjectInfo::GetIObjectControl","cos.imanagedobjectinfo_getiobjectcontrol"]
old-location: cos\imanagedobjectinfo_getiobjectcontrol.htm
tech.root: cos
ms.assetid: 0ce1408a-488e-4705-8155-445e1be8c51f
ms.date: 12/05/2018
ms.keywords: GetIObjectControl, GetIObjectControl method [COM+], GetIObjectControl method [COM+],IManagedObjectInfo interface, IManagedObjectInfo interface [COM+],GetIObjectControl method, IManagedObjectInfo.GetIObjectControl, IManagedObjectInfo::GetIObjectControl, _cos_IManagedObjectInfo_GetIObjectControl, comsvcs/IManagedObjectInfo::GetIObjectControl, cos.imanagedobjectinfo_getiobjectcontrol
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
 - IManagedObjectInfo::GetIObjectControl
 - comsvcs/IManagedObjectInfo::GetIObjectControl
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
 - IManagedObjectInfo.GetIObjectControl
---

# IManagedObjectInfo::GetIObjectControl


## -description

Retrieves the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a> interface that is associated with the managed object.

## -parameters

### -param pCtrl [out]

A reference to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedobjectinfo">IManagedObjectInfo</a>