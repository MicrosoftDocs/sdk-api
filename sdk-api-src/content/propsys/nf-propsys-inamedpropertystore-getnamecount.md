---
UID: NF:propsys.INamedPropertyStore.GetNameCount
title: INamedPropertyStore::GetNameCount (propsys.h)
description: Gets the number of property names in the property store.
helpviewer_keywords: ["GetNameCount","GetNameCount method [Windows Shell]","GetNameCount method [Windows Shell]","INamedPropertyStore interface","INamedPropertyStore interface [Windows Shell]","GetNameCount method","INamedPropertyStore.GetNameCount","INamedPropertyStore::GetNameCount","_shell_INamedPropertyStore_GetNameCount","propsys/INamedPropertyStore::GetNameCount","shell.INamedPropertyStore_GetNameCount"]
old-location: shell\INamedPropertyStore_GetNameCount.htm
tech.root: shell
ms.assetid: 74bba1bf-e003-40bb-9118-4d647f78e409
ms.date: 12/05/2018
ms.keywords: GetNameCount, GetNameCount method [Windows Shell], GetNameCount method [Windows Shell],INamedPropertyStore interface, INamedPropertyStore interface [Windows Shell],GetNameCount method, INamedPropertyStore.GetNameCount, INamedPropertyStore::GetNameCount, _shell_INamedPropertyStore_GetNameCount, propsys/INamedPropertyStore::GetNameCount, shell.INamedPropertyStore_GetNameCount
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
 - INamedPropertyStore::GetNameCount
 - propsys/INamedPropertyStore::GetNameCount
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
 - INamedPropertyStore.GetNameCount
---

# INamedPropertyStore::GetNameCount


## -description

Gets the number of property names in the property store.

## -parameters

### -param pdwCount [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to the count of names.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

