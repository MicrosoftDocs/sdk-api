---
UID: NF:dinputd.IDirectInputEffectDriver.QueryInterface
title: IDirectInputEffectDriver::QueryInterface method
author: windows-driver-content
description: The IDirectInputEffectDriver::QueryInterface method determines whether the DirectInputEffectDriver object supports a particular COM interface.
old-location: hid\idirectinputeffectdriver_queryinterface.htm
old-project: hid
ms.assetid: 8a9c1279-c25f-48a4-8bd2-65bffe40cd63
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: IDirectInputEffectDriver, IDirectInputEffectDriver interface [Human Input Devices], QueryInterface method, IDirectInputEffectDriver::QueryInterface, QueryInterface method [Human Input Devices], QueryInterface method [Human Input Devices], IDirectInputEffectDriver interface, QueryInterface,IDirectInputEffectDriver.QueryInterface, di_ref_99e25056-d0d2-464f-81b4-cfa6bdfa06db.xml, dinputd/IDirectInputEffectDriver::QueryInterface, hid.idirectinputeffectdriver_queryinterface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DIEFFESCAPE, *LPDIEFFESCAPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dinputd.h
api_name:
-	IDirectInputEffectDriver.QueryInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectInputEffectDriver::QueryInterface method


## -description


The <b>IDirectInputEffectDriver::QueryInterface </b>method determines whether the DirectInputEffectDriver object supports a particular COM interface. If it does, the system increases the reference count for the object by 1, and the application can begin using that interface immediately. This method is part of the <b>IUnknown</b> interface inherited by DirectInputEffectDriver. 


## -parameters




### -param riid

Reference identifier of the interface being requested. 


### -param ppvObj

Address of a pointer to be filled with the interface pointer if the query is successful. 


## -returns



Returns S_OK if the interface is supported; otherwise, returns E_NOINTERFACE.




## -remarks



When the application no longer needs to use the interface retrieved by a call to this method, it must call the <b>Release</b> method for that interface to free it. 



