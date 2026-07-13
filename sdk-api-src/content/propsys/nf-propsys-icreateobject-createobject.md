---
UID: NF:propsys.ICreateObject.CreateObject
title: ICreateObject::CreateObject (propsys.h)
description: Creates a local object of a specified class and returns a pointer to a specified interface on the object.
helpviewer_keywords: ["CreateObject","CreateObject method [Windows Shell]","CreateObject method [Windows Shell]","ICreateObject interface","ICreateObject interface [Windows Shell]","CreateObject method","ICreateObject.CreateObject","ICreateObject::CreateObject","_shell_ICreateObject_CreateObject","propsys/ICreateObject::CreateObject","shell.ICreateObject_CreateObject"]
old-location: shell\ICreateObject_CreateObject.htm
tech.root: shell
ms.assetid: 72c56de7-4c04-4bcf-b6bb-6e41d12b68a3
ms.date: 12/05/2018
ms.keywords: CreateObject, CreateObject method [Windows Shell], CreateObject method [Windows Shell],ICreateObject interface, ICreateObject interface [Windows Shell],CreateObject method, ICreateObject.CreateObject, ICreateObject::CreateObject, _shell_ICreateObject_CreateObject, propsys/ICreateObject::CreateObject, shell.ICreateObject_CreateObject
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - ICreateObject::CreateObject
 - propsys/ICreateObject::CreateObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - ICreateObject.CreateObject
---

# ICreateObject::CreateObject


## -description

Creates a local object of a specified class and returns a pointer to a specified interface on the object.

## -parameters

### -param clsid [in]

Type: <b>REFCLSID</b>

A reference to a CLSID.

### -param pUnkOuter [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface that aggregates the object created by this function, or <b>NULL</b> if no aggregation is desired.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface the created object should return.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of the pointer to the interface requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be used with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystorewithcreateobject">GetPropertyStoreWithCreateObject</a>.