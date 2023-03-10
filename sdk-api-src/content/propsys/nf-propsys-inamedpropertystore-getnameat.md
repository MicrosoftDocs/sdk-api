---
UID: NF:propsys.INamedPropertyStore.GetNameAt
title: INamedPropertyStore::GetNameAt (propsys.h)
description: Gets the name of a property at a specified index in the property store.
helpviewer_keywords: ["GetNameAt","GetNameAt method [Windows Shell]","GetNameAt method [Windows Shell]","INamedPropertyStore interface","INamedPropertyStore interface [Windows Shell]","GetNameAt method","INamedPropertyStore.GetNameAt","INamedPropertyStore::GetNameAt","_shell_INamedPropertyStore_GetNameAt","propsys/INamedPropertyStore::GetNameAt","shell.INamedPropertyStore_GetNameAt"]
old-location: shell\INamedPropertyStore_GetNameAt.htm
tech.root: shell
ms.assetid: 2fd3896e-b170-49af-811e-a1f2facc7a84
ms.date: 12/05/2018
ms.keywords: GetNameAt, GetNameAt method [Windows Shell], GetNameAt method [Windows Shell],INamedPropertyStore interface, INamedPropertyStore interface [Windows Shell],GetNameAt method, INamedPropertyStore.GetNameAt, INamedPropertyStore::GetNameAt, _shell_INamedPropertyStore_GetNameAt, propsys/INamedPropertyStore::GetNameAt, shell.INamedPropertyStore_GetNameAt
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
 - INamedPropertyStore::GetNameAt
 - propsys/INamedPropertyStore::GetNameAt
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
 - INamedPropertyStore.GetNameAt
---

# INamedPropertyStore::GetNameAt


## -description

Gets the name of a property at a specified index in the property store.

## -parameters

### -param iProp [in]

Type: <b>DWORD</b>

The index of the property in the store.

### -param pbstrName [out]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>*</b>

When this method returns, contains a pointer to the property's name. It is the calling application's responsibility to free this resource when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.