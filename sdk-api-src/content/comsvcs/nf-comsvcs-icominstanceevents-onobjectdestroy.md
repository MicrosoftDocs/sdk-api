---
UID: NF:comsvcs.IComInstanceEvents.OnObjectDestroy
title: IComInstanceEvents::OnObjectDestroy method
author: windows-driver-content
description: Generated when an object is released by a client.
old-location: cos\icominstanceevents_onobjectdestroy.htm
old-project: cossdk
ms.assetid: 3eea4171-a177-4adc-bd9a-856a558ba3d8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IComInstanceEvents, IComInstanceEvents interface [COM+], OnObjectDestroy method, IComInstanceEvents::OnObjectDestroy, OnObjectDestroy method [COM+], OnObjectDestroy method [COM+], IComInstanceEvents interface, OnObjectDestroy,IComInstanceEvents.OnObjectDestroy, _dtc_IComInstanceEvents_OnObjectDestroy, comsvcs/IComInstanceEvents::OnObjectDestroy, cos.icominstanceevents_onobjectdestroy
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
-	IComInstanceEvents.OnObjectDestroy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComInstanceEvents::OnObjectDestroy method


## -description


Generated when an object is released by a client.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param CtxtID [in]

The context identifier of the object.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/11e4559e-04c5-4fa9-b618-458ca7daf00e">IComInstanceEvents</a>
 

 

