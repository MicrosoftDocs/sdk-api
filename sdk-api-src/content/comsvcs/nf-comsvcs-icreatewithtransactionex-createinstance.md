---
UID: NF:comsvcs.ICreateWithTransactionEx.CreateInstance
title: ICreateWithTransactionEx::CreateInstance (comsvcs.h)
description: Creates a COM+ object that executes within the scope of a manual transaction specified with a reference to an ITransaction interface.
helpviewer_keywords: ["CreateInstance","CreateInstance method [COM+]","CreateInstance method [COM+]","ICreateWithTransactionEx interface","ICreateWithTransactionEx interface [COM+]","CreateInstance method","ICreateWithTransactionEx.CreateInstance","ICreateWithTransactionEx::CreateInstance","_dtc_ICreateWithTransactionEx_CreateInstance","comsvcs/ICreateWithTransactionEx::CreateInstance","cos.icreatewithtransactionex_createinstance"]
old-location: cos\icreatewithtransactionex_createinstance.htm
tech.root: cos
ms.assetid: 71d3b8ad-195b-47a6-8197-05df6311ed2a
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [COM+], CreateInstance method [COM+],ICreateWithTransactionEx interface, ICreateWithTransactionEx interface [COM+],CreateInstance method, ICreateWithTransactionEx.CreateInstance, ICreateWithTransactionEx::CreateInstance, _dtc_ICreateWithTransactionEx_CreateInstance, comsvcs/ICreateWithTransactionEx::CreateInstance, cos.icreatewithtransactionex_createinstance
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICreateWithTransactionEx::CreateInstance
 - comsvcs/ICreateWithTransactionEx::CreateInstance
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
 - ICreateWithTransactionEx.CreateInstance
---

# ICreateWithTransactionEx::CreateInstance


## -description

Creates a COM+ object that executes within the scope of a manual transaction specified with a reference to an <b>ITransaction</b> interface.

## -parameters

### -param pTransaction [in]

An <b>ITransaction</b> interface pointer indicating the transaction in which you want to create the COM+ object.

### -param rclsid [in]

The CLSID of the type of object to instantiate.

### -param riid [in]

The ID of the interface to be returned by the <i>ppvObj</i> parameter.

### -param pObject [out]

A new object of the type specified by the <i>rclsid</i> argument through the interface specified by the <i>riid</i> argument.

## -returns

This method can return the following values:

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icreatewithtransactionex">ICreateWithTransactionEx</a>