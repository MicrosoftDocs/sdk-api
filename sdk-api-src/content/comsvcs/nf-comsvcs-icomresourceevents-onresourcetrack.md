---
UID: NF:comsvcs.IComResourceEvents.OnResourceTrack
title: IComResourceEvents::OnResourceTrack
author: windows-sdk-content
description: Generated when a resource is tracked.
old-location: cos\icomresourceevents_onresourcetrack.htm
tech.root: cossdk
ms.assetid: 8845cf07-f796-45bd-9d3d-261cf0903050
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComResourceEvents interface [COM+],OnResourceTrack method, IComResourceEvents.OnResourceTrack, IComResourceEvents::OnResourceTrack, OnResourceTrack, OnResourceTrack method [COM+], OnResourceTrack method [COM+],IComResourceEvents interface, _dtc_IComResourceEvents_OnResourceTrack, comsvcs/IComResourceEvents::OnResourceTrack, cos.icomresourceevents_onresourcetrack
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
 - IComResourceEvents.OnResourceTrack
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComResourceEvents::OnResourceTrack


## -description


Generated when a resource is tracked.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


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




<a href="https://msdn.microsoft.com/fdc664b6-0459-4cbd-8e9e-0c3fe82e4321">IComResourceEvents</a>
 

 

