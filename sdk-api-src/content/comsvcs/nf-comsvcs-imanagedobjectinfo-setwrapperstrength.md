---
UID: NF:comsvcs.IManagedObjectInfo.SetWrapperStrength
title: IManagedObjectInfo::SetWrapperStrength
author: windows-sdk-content
description: Sets whether the managed object holds a strong or a weak reference to the COM+ context.
old-location: cos\imanagedobjectinfo_setwrapperstrength.htm
old-project: cossdk
ms.assetid: 0f03c6cb-4bfc-4871-8f5b-78ccc8df8838
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IManagedObjectInfo interface [COM+],SetWrapperStrength method, IManagedObjectInfo.SetWrapperStrength, IManagedObjectInfo::SetWrapperStrength, SetWrapperStrength, SetWrapperStrength method [COM+], SetWrapperStrength method [COM+],IManagedObjectInfo interface, _cos_IManagedObjectInfo_SetWrapperStrength, comsvcs/IManagedObjectInfo::SetWrapperStrength, cos.imanagedobjectinfo_setwrapperstrength
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IManagedObjectInfo.SetWrapperStrength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IManagedObjectInfo::SetWrapperStrength


## -description


Sets whether the managed object holds a strong or a weak reference to the COM+ context.


## -parameters




### -param bStrong [in]

Indicates whether the managed object holds a strong or a weak reference to the COM+ context. A strong reference keeps the object alive and prevents it from being destroyed during garbage collection.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/7fa5f76e-df07-41b3-8fb0-62b84a034aa5">IManagedObjectInfo</a>
 

 

