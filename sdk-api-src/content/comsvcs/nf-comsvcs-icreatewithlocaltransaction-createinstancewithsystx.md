---
UID: NF:comsvcs.ICreateWithLocalTransaction.CreateInstanceWithSysTx
title: ICreateWithLocalTransaction::CreateInstanceWithSysTx (comsvcs.h)
description: Creates a COM+ object that executes within the scope of the specified local transaction. (ICreateWithLocalTransaction.CreateInstanceWithSysTx)
helpviewer_keywords: ["CreateInstanceWithSysTx","CreateInstanceWithSysTx method [COM+]","CreateInstanceWithSysTx method [COM+]","ICreateWithLocalTransaction interface","ICreateWithLocalTransaction interface [COM+]","CreateInstanceWithSysTx method","ICreateWithLocalTransaction.CreateInstanceWithSysTx","ICreateWithLocalTransaction::CreateInstanceWithSysTx","comsvcs/ICreateWithLocalTransaction::CreateInstanceWithSysTx","cos.icreatewithlocaltransaction_createinstancewithsystx"]
old-location: cos\icreatewithlocaltransaction_createinstancewithsystx.htm
tech.root: cos
ms.assetid: e56a1810-77e7-47fa-b8b1-bb1ebc5662fd
ms.date: 12/05/2018
ms.keywords: CreateInstanceWithSysTx, CreateInstanceWithSysTx method [COM+], CreateInstanceWithSysTx method [COM+],ICreateWithLocalTransaction interface, ICreateWithLocalTransaction interface [COM+],CreateInstanceWithSysTx method, ICreateWithLocalTransaction.CreateInstanceWithSysTx, ICreateWithLocalTransaction::CreateInstanceWithSysTx, comsvcs/ICreateWithLocalTransaction::CreateInstanceWithSysTx, cos.icreatewithlocaltransaction_createinstancewithsystx
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICreateWithLocalTransaction::CreateInstanceWithSysTx
 - comsvcs/ICreateWithLocalTransaction::CreateInstanceWithSysTx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICreateWithLocalTransaction.CreateInstanceWithSysTx
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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icreatewithlocaltransaction">ICreateWithLocalTransaction</a>
