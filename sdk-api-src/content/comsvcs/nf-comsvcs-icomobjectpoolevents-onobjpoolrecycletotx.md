---
UID: NF:comsvcs.IComObjectPoolEvents.OnObjPoolRecycleToTx
title: IComObjectPoolEvents::OnObjPoolRecycleToTx (comsvcs.h)
author: windows-sdk-content
description: Generated when a transactional object is returned to the pool.
old-location: cos\icomobjectpoolevents_onobjpoolrecycletotx.htm
tech.root: cossdk
ms.assetid: 6acae10b-9fda-4c73-b781-62a480271fd1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents interface [COM+],OnObjPoolRecycleToTx method, IComObjectPoolEvents.OnObjPoolRecycleToTx, IComObjectPoolEvents::OnObjPoolRecycleToTx, OnObjPoolRecycleToTx, OnObjPoolRecycleToTx method [COM+], OnObjPoolRecycleToTx method [COM+],IComObjectPoolEvents interface, _dtc_icomobjectpoolevents_onobjpoolrecycletotx, comsvcs/IComObjectPoolEvents::OnObjPoolRecycleToTx, cos.icomobjectpoolevents_onobjpoolrecycletotx
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
 - IComObjectPoolEvents.OnObjPoolRecycleToTx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComObjectPoolEvents::OnObjPoolRecycleToTx


## -description


Generated when a transactional object is returned to the pool.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The activity ID for which the object is created.


### -param guidObject [in]

The CLSID for the objects in the pool.


### -param guidTx [in]

The GUID representing the transaction identifier.


### -param objid [in]

The unique identifier for this object.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/a830b40b-a1b1-464e-b532-91cebd4e5d2f">IComObjectPoolEvents</a>
 

 

