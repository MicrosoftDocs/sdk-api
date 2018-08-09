---
UID: NF:comsvcs.IComObjectConstructionEvents.OnObjectConstruct
title: IComObjectConstructionEvents::OnObjectConstruct
author: windows-sdk-content
description: Generated when a constructed object is created.
old-location: cos\icomobjectconstructionevents_onobjectconstruct.htm
old-project: cossdk
ms.assetid: 8a90e561-79a0-4490-bbc8-f376e4278ab9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IComObjectConstructionEvents interface [COM+],OnObjectConstruct method, IComObjectConstructionEvents.OnObjectConstruct, IComObjectConstructionEvents::OnObjectConstruct, OnObjectConstruct, OnObjectConstruct method [COM+], OnObjectConstruct method [COM+],IComObjectConstructionEvents interface, _dtc_IComObjectConstructionEvents_OnObjectConstruct, comsvcs/IComObjectConstructionEvents::OnObjectConstruct, cos.icomobjectconstructionevents_onobjectconstruct
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
 - IComObjectConstructionEvents.OnObjectConstruct
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectConstructionEvents::OnObjectConstruct


## -description


Generated when a constructed object is created.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidObject [in]

The CLSID for the objects in the pool.


### -param sConstructString [in]

The object construction string.


### -param oid [in]

The unique constructed object identifier.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/c5fdb9b1-937e-43cb-93ff-e90f8c268fee">IComObjectConstructionEvents</a>
 

 

