---
UID: NF:comsvcs.IComInstanceEvents.OnObjectCreate
title: IComInstanceEvents::OnObjectCreate
author: windows-sdk-content
description: Generated when an object is created by a client.
old-location: cos\icominstanceevents_onobjectcreate.htm
tech.root: cossdk
ms.assetid: 4f3457f6-4956-4411-b38b-46c7d84d342d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComInstanceEvents interface [COM+],OnObjectCreate method, IComInstanceEvents.OnObjectCreate, IComInstanceEvents::OnObjectCreate, OnObjectCreate, OnObjectCreate method [COM+], OnObjectCreate method [COM+],IComInstanceEvents interface, _dtc_icominstanceevents_onobjectcreate, comsvcs/IComInstanceEvents::OnObjectCreate, cos.icominstanceevents_onobjectcreate
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
 - IComInstanceEvents.OnObjectCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComInstanceEvents::OnObjectCreate


## -description


Generated when an object is created by a client.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The identifier of the activity in which the object is created.


### -param clsid [in]

The CLSID of the object being created.


### -param tsid [in]

The transaction stream identifier, which is unique for correlation to objects.


### -param CtxtID [in]

The context identifier for this object.


### -param ObjectID [in]

The initial just-in-time (JIT) activated object.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/11e4559e-04c5-4fa9-b618-458ca7daf00e">IComInstanceEvents</a>
 

 

