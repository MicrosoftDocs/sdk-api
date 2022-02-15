---
UID: NF:objectarray.IObjectCollection.AddObject
title: IObjectCollection::AddObject (objectarray.h)
description: Adds a single object to the collection.
helpviewer_keywords: ["AddObject","AddObject method [Windows Shell]","AddObject method [Windows Shell]","IObjectCollection interface","IObjectCollection interface [Windows Shell]","AddObject method","IObjectCollection.AddObject","IObjectCollection::AddObject","_shell_IObjectCollection_AddObject","objectarray/IObjectCollection::AddObject","shell.IObjectCollection_AddObject"]
old-location: shell\IObjectCollection_AddObject.htm
tech.root: shell
ms.assetid: 0898160d-46e5-4b38-9fc9-f74bd6a0385b
ms.date: 12/05/2018
ms.keywords: AddObject, AddObject method [Windows Shell], AddObject method [Windows Shell],IObjectCollection interface, IObjectCollection interface [Windows Shell],AddObject method, IObjectCollection.AddObject, IObjectCollection::AddObject, _shell_IObjectCollection_AddObject, objectarray/IObjectCollection::AddObject, shell.IObjectCollection_AddObject
req.header: objectarray.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IObjectCollection::AddObject
 - objectarray/IObjectCollection::AddObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objectarray.h
api_name:
 - IObjectCollection.AddObject
---

# IObjectCollection::AddObject


## -description

Adds a single object to the collection.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the object to be added to the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.