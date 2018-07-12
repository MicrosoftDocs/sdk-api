---
UID: NF:comsvcs.IComObjectPoolEvents2.OnObjPoolTimeout
title: IComObjectPoolEvents2::OnObjPoolTimeout
author: windows-sdk-content
description: Generated when the request for a pooled object times out.
old-location: cos\icomobjectpoolevents2_onobjpooltimeout.htm
old-project: cossdk
ms.assetid: a5468ae6-6c7e-4ae1-afbc-24cc9b08102f
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IComObjectPoolEvents2 interface [COM+],OnObjPoolTimeout method, IComObjectPoolEvents2.OnObjPoolTimeout, IComObjectPoolEvents2::OnObjPoolTimeout, OnObjPoolTimeout, OnObjPoolTimeout method [COM+], OnObjPoolTimeout method [COM+],IComObjectPoolEvents2 interface, _dtc_IComObjectPoolEvents2_OnObjPoolTimeout, comsvcs/IComObjectPoolEvents2::OnObjPoolTimeout, cos.icomobjectpoolevents2_onobjpooltimeout
ms.prod: windows
ms.technology: windows-sdk
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
 - IComObjectPoolEvents2.OnObjPoolTimeout
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectPoolEvents2::OnObjPoolTimeout


## -description


Generated when the request for a pooled object times out.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidObject [in]

The CLSID for the objects in the pool.


### -param guidActivity [in]

The identifier of the activity in which the object is created.


### -param dwTimeout [in]

The pool's time-out value.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/f1891d8b-e3d0-4378-ac67-c2c0ddd65602">IComObjectPoolEvents2</a>
 

 

