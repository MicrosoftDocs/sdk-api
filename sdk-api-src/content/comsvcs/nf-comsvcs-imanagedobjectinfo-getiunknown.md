---
UID: NF:comsvcs.IManagedObjectInfo.GetIUnknown
title: IManagedObjectInfo::GetIUnknown method
author: windows-driver-content
description: Retrieves the IUnknown interface that is associated with the managed object.
old-location: cos\imanagedobjectinfo_getiunknown.htm
old-project: cossdk
ms.assetid: 1c0d27cb-1725-4654-ab15-0ef815ce6657
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetIUnknown method [COM+], GetIUnknown method [COM+], IManagedObjectInfo interface, GetIUnknown,IManagedObjectInfo.GetIUnknown, IManagedObjectInfo, IManagedObjectInfo interface [COM+], GetIUnknown method, IManagedObjectInfo::GetIUnknown, _cos_IManagedObjectInfo_GetIUnknown, comsvcs/IManagedObjectInfo::GetIUnknown, cos.imanagedobjectinfo_getiunknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IManagedObjectInfo.GetIUnknown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IManagedObjectInfo::GetIUnknown method


## -description


Retrieves the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface that is associated with the managed object.


## -parameters




### -param pUnk [out]

A reference to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/7fa5f76e-df07-41b3-8fb0-62b84a034aa5">IManagedObjectInfo</a>
 

 

