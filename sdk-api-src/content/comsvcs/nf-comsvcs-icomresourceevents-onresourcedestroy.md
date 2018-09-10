---
UID: NF:comsvcs.IComResourceEvents.OnResourceDestroy
title: IComResourceEvents::OnResourceDestroy
author: windows-sdk-content
description: Generated when a resource is destroyed.
old-location: cos\icomresourceevents_onresourcedestroy.htm
tech.root: cossdk
ms.assetid: cc934b47-8031-4dab-ae00-6389f54749b8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComResourceEvents interface [COM+],OnResourceDestroy method, IComResourceEvents.OnResourceDestroy, IComResourceEvents::OnResourceDestroy, OnResourceDestroy, OnResourceDestroy method [COM+], OnResourceDestroy method [COM+],IComResourceEvents interface, _dtc_IComResourceEvents_OnResourceDestroy, comsvcs/IComResourceEvents::OnResourceDestroy, cos.icomresourceevents_onresourcedestroy
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComResourceEvents.OnResourceDestroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComResourceEvents::OnResourceDestroy


## -description


Generated when a resource is destroyed.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param ObjectID [in]

The just-in-time activated object.


### -param hr [in]

The result from resource dispensers destroy call.


### -param pszType [in]

A description of the resource.


### -param resId [in]

The unique identifier of the resource.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/fdc664b6-0459-4cbd-8e9e-0c3fe82e4321">IComResourceEvents</a>
 

 

