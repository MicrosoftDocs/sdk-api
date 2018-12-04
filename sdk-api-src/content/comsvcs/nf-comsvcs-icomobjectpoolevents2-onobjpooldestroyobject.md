---
UID: NF:comsvcs.IComObjectPoolEvents2.OnObjPoolDestroyObject
title: IComObjectPoolEvents2::OnObjPoolDestroyObject
author: windows-sdk-content
description: Generated when an object is permanently removed from the pool.
old-location: cos\icomobjectpoolevents2_onobjpooldestroyobject.htm
tech.root: cossdk
ms.assetid: c942da45-4d41-4483-a30b-862d3e0c13b7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IComObjectPoolEvents2 interface [COM+],OnObjPoolDestroyObject method, IComObjectPoolEvents2.OnObjPoolDestroyObject, IComObjectPoolEvents2::OnObjPoolDestroyObject, OnObjPoolDestroyObject, OnObjPoolDestroyObject method [COM+], OnObjPoolDestroyObject method [COM+],IComObjectPoolEvents2 interface, _dtc_IComObjectPoolEvents2_OnObjPoolDestroyObject, comsvcs/IComObjectPoolEvents2::OnObjPoolDestroyObject, cos.icomobjectpoolevents2_onobjpooldestroyobject
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
 - IComObjectPoolEvents2.OnObjPoolDestroyObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectPoolEvents2::OnObjPoolDestroyObject


## -description


Generated when an object is permanently removed from the pool.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidObject [in]

The CLSID for the objects in the pool.


### -param dwObjsCreated [in]

The number of objects in the pool.


### -param oid [in]

The unique pooled object identifier.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/f1891d8b-e3d0-4378-ac67-c2c0ddd65602">IComObjectPoolEvents2</a>
 

 

