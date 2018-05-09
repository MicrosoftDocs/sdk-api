---
UID: NF:comsvcs.ICreateWithLocalTransaction.CreateInstanceWithSysTx
title: ICreateWithLocalTransaction::CreateInstanceWithSysTx
author: windows-driver-content
description: Creates a COM+ object that executes within the scope of the specified local transaction.
old-location: cos\icreatewithlocaltransaction_createinstancewithsystx.htm
old-project: cossdk
ms.assetid: e56a1810-77e7-47fa-b8b1-bb1ebc5662fd
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: CreateInstanceWithSysTx, CreateInstanceWithSysTx method [COM+], CreateInstanceWithSysTx method [COM+],ICreateWithLocalTransaction interface, ICreateWithLocalTransaction interface [COM+],CreateInstanceWithSysTx method, ICreateWithLocalTransaction.CreateInstanceWithSysTx, ICreateWithLocalTransaction::CreateInstanceWithSysTx, comsvcs/ICreateWithLocalTransaction::CreateInstanceWithSysTx, cos.icreatewithlocaltransaction_createinstancewithsystx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
-	ICreateWithLocalTransaction.CreateInstanceWithSysTx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICreateWithLocalTransaction::CreateInstanceWithSysTx


## -description


Creates a COM+ object that executes within the scope of the specified local transaction.


## -parameters




### -param pTransaction [in]

The transaction in which the requested object participates.


### -param rclsid [in]

The CLSID of the class from which to create the requested object.


### -param riid [in]

A reference to the interface identifier (IID) of the interface that is used to communicate with the request object.


### -param pObject [out, retval]

The address of the pointer variable that receives the interface pointer specified with <i>riid</i>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/667ebc77-943c-4cf0-90b4-7c28949f406e">ICreateWithLocalTransaction</a>
 

 

