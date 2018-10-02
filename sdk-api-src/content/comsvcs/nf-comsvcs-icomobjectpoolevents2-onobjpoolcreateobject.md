---
UID: NF:comsvcs.IComObjectPoolEvents2.OnObjPoolCreateObject
title: IComObjectPoolEvents2::OnObjPoolCreateObject
author: windows-sdk-content
description: Generated when an object is created for the pool.
old-location: cos\icomobjectpoolevents2_onobjpoolcreateobject.htm
tech.root: cossdk
ms.assetid: 85e50bf4-2660-409c-8812-cbe389283202
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComObjectPoolEvents2 interface [COM+],OnObjPoolCreateObject method, IComObjectPoolEvents2.OnObjPoolCreateObject, IComObjectPoolEvents2::OnObjPoolCreateObject, OnObjPoolCreateObject, OnObjPoolCreateObject method [COM+], OnObjPoolCreateObject method [COM+],IComObjectPoolEvents2 interface, _dtc_IComObjectPoolEvents2_OnObjPoolCreateObject, comsvcs/IComObjectPoolEvents2::OnObjPoolCreateObject, cos.icomobjectpoolevents2_onobjpoolcreateobject
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
 - IComObjectPoolEvents2.OnObjPoolCreateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectPoolEvents2::OnObjPoolCreateObject


## -description


Generated when an object is created for the pool.


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
 

 

