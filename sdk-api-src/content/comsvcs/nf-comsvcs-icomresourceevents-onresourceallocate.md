---
UID: NF:comsvcs.IComResourceEvents.OnResourceAllocate
title: IComResourceEvents::OnResourceAllocate method
author: windows-driver-content
description: Generated when an existing resource is allocated.
old-location: cos\icomresourceevents_onresourceallocate.htm
old-project: cossdk
ms.assetid: f063230d-a0b8-46c5-845c-f94aefb706a7
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComResourceEvents, IComResourceEvents interface [COM+], OnResourceAllocate method, IComResourceEvents::OnResourceAllocate, OnResourceAllocate method [COM+], OnResourceAllocate method [COM+], IComResourceEvents interface, OnResourceAllocate,IComResourceEvents.OnResourceAllocate, _dtc_IComResourceEvents_OnResourceAllocate, comsvcs/IComResourceEvents::OnResourceAllocate, cos.icomresourceevents_onresourceallocate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComResourceEvents.OnResourceAllocate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComResourceEvents::OnResourceAllocate method


## -description


Generated when an existing resource is allocated.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


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




<a href="https://msdn.microsoft.com/fdc664b6-0459-4cbd-8e9e-0c3fe82e4321">IComResourceEvents</a>
 

 

