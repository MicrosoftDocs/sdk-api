---
UID: NF:comsvcs.IComInstance2Events.OnObjectDestroy2
title: IComInstance2Events::OnObjectDestroy2
author: windows-driver-content
description: Generated when a client releases an object.
old-location: cos\icominstance2events_onobjectdestroy2.htm
old-project: cossdk
ms.assetid: eeaf62b1-4c25-4232-829b-b2b147575ce9
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IComInstance2Events interface [COM+],OnObjectDestroy2 method, IComInstance2Events.OnObjectDestroy2, IComInstance2Events::OnObjectDestroy2, OnObjectDestroy2, OnObjectDestroy2 method [COM+], OnObjectDestroy2 method [COM+],IComInstance2Events interface, _dtc_IComInstance2Events_OnObjectDestroy2, comsvcs/IComInstance2Events::OnObjectDestroy2, cos.icominstance2events_onobjectdestroy2
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
-	IComInstance2Events.OnObjectDestroy2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComInstance2Events::OnObjectDestroy2


## -description


Generated when a client releases an object.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param CtxtID [in]

The context identifier of the object.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/2fb2904d-7069-4303-bb3c-2caef9499c1e">IComInstance2Events</a>
 

 

