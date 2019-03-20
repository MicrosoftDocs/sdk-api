---
UID: NF:comsvcs.IComObjectPoolEvents.OnObjPoolGetFromTx
title: IComObjectPoolEvents::OnObjPoolGetFromTx (comsvcs.h)
author: windows-sdk-content
description: Generated when a transactional object is obtained from the pool.
old-location: cos\icomobjectpoolevents_onobjpoolgetfromtx.htm
tech.root: cossdk
ms.assetid: 977ab640-a9d5-47f5-ad47-ad2e1648fd6b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComObjectPoolEvents interface [COM+],OnObjPoolGetFromTx method, IComObjectPoolEvents.OnObjPoolGetFromTx, IComObjectPoolEvents::OnObjPoolGetFromTx, OnObjPoolGetFromTx, OnObjPoolGetFromTx method [COM+], OnObjPoolGetFromTx method [COM+],IComObjectPoolEvents interface, _dtc_IComObjectPoolEvents_OnObjPoolGetFromTx, comsvcs/IComObjectPoolEvents::OnObjPoolGetFromTx, cos.icomobjectpoolevents_onobjpoolgetfromtx
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
 - IComObjectPoolEvents.OnObjPoolGetFromTx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectPoolEvents::OnObjPoolGetFromTx


## -description


Generated when a transactional object is obtained from the pool.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The activity ID for which the object is created.


### -param guidObject [in]

The CLSID for the objects in the pool.


### -param guidTx [in]

The transaction identifier.


### -param objid [in]

The unique identifier for this object.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/a830b40b-a1b1-464e-b532-91cebd4e5d2f">IComObjectPoolEvents</a>
 

 

