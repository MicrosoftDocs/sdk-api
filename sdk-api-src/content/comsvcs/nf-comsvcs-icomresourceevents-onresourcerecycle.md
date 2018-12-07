---
UID: NF:comsvcs.IComResourceEvents.OnResourceRecycle
title: IComResourceEvents::OnResourceRecycle
author: windows-sdk-content
description: Generated when an object is finished with a resource.
old-location: cos\icomresourceevents_onresourcerecycle.htm
tech.root: cossdk
ms.assetid: 615e0f73-2935-4ef3-94c9-5c74b5c82db4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComResourceEvents interface [COM+],OnResourceRecycle method, IComResourceEvents.OnResourceRecycle, IComResourceEvents::OnResourceRecycle, OnResourceRecycle, OnResourceRecycle method [COM+], OnResourceRecycle method [COM+],IComResourceEvents interface, _dtc_IComResourceEvents_OnResourceRecycle, comsvcs/IComResourceEvents::OnResourceRecycle, cos.icomresourceevents_onresourcerecycle
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
 - IComResourceEvents.OnResourceRecycle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComResourceEvents::OnResourceRecycle


## -description


Generated when an object is finished with a resource.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param ObjectID [in]

The just-in-time activated object.


### -param pszType [in]

A description of the resource.


### -param resId [in]

The unique identifier of the resource.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/fdc664b6-0459-4cbd-8e9e-0c3fe82e4321">IComResourceEvents</a>
 

 

