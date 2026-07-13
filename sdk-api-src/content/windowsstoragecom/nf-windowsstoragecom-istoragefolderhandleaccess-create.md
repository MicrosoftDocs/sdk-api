---
UID: NF:windowsstoragecom.IStorageFolderHandleAccess.Create
title: IStorageFolderHandleAccess::Create (windowsstoragecom.h)
description: Creates a handle to a file that is in a storage folder.
helpviewer_keywords: ["Create","Create method [Windows Runtime]","Create method [Windows Runtime]","IStorageFolderHandleAccess interface","IStorageFolderHandleAccess interface [Windows Runtime]","Create method","IStorageFolderHandleAccess.Create","IStorageFolderHandleAccess::Create","windowsstoragecom/IStorageFolderHandleAccess::Create","winrt.istoragefolderhandleaccess_create"]
old-location: winrt\istoragefolderhandleaccess_create.htm
tech.root: WinRT
ms.assetid: CAA79CEC-FB04-48F0-BCF8-19613FA6D108
ms.date: 12/05/2018
ms.keywords: Create, Create method [Windows Runtime], Create method [Windows Runtime],IStorageFolderHandleAccess interface, IStorageFolderHandleAccess interface [Windows Runtime],Create method, IStorageFolderHandleAccess.Create, IStorageFolderHandleAccess::Create, windowsstoragecom/IStorageFolderHandleAccess::Create, winrt.istoragefolderhandleaccess_create
req.header: windowsstoragecom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WindowsStorageCOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Windows.storage.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStorageFolderHandleAccess::Create
 - windowsstoragecom/IStorageFolderHandleAccess::Create
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.storage.dll
api_name:
 - IStorageFolderHandleAccess.Create
---

# IStorageFolderHandleAccess::Create


## -description

Creates a handle to a file that is  in a storage folder.

## -parameters

### -param fileName [in]

The name of the file that you want to get a handle to.

### -param creationOptions [in]

The action to take on a file that exists or doesn't exist.

### -param accessOptions [in]

The level of access that a handle has on the file.

### -param sharingOptions [in]

The requested sharing mode of the handle.

### -param options [in]

The flags of the file handle.

### -param oplockBreakingHandler [in, optional]

Not currently implemented.

### -param interopHandle [out, retval]

The handle to the file.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istoragefolderhandleaccess">IStorageFolderHandleAccess</a>