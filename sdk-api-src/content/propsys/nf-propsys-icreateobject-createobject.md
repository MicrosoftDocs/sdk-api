---
UID: NF:propsys.ICreateObject.CreateObject
title: ICreateObject::CreateObject
author: windows-sdk-content
description: Creates a local object of a specified class and returns a pointer to a specified interface on the object.
old-location: shell\ICreateObject_CreateObject.htm
old-project: shell
ms.assetid: 72c56de7-4c04-4bcf-b6bb-6e41d12b68a3
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CreateObject, CreateObject method [Windows Shell], CreateObject method [Windows Shell],ICreateObject interface, ICreateObject interface [Windows Shell],CreateObject method, ICreateObject.CreateObject, ICreateObject::CreateObject, _shell_ICreateObject_CreateObject, propsys/ICreateObject::CreateObject, shell.ICreateObject_CreateObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propsys.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - ICreateObject.CreateObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateObject::CreateObject


## -description


Creates a local object of a specified class and returns a pointer to a specified interface on the object.


## -parameters




### -param clsid [in]

Type: <b>REFCLSID</b>

A reference to a CLSID.


### -param pUnkOuter [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface that aggregates the object created by this function, or <b>NULL</b> if no aggregation is desired.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface the created object should return.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of the pointer to the interface requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be used with <a href="https://msdn.microsoft.com/6a90ea62-e4d7-4876-802a-9c1f6c296714">GetPropertyStoreWithCreateObject</a>.



