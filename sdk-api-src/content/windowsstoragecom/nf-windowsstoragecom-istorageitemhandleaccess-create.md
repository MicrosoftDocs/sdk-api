---
UID: NF:windowsstoragecom.IStorageItemHandleAccess.Create
title: IStorageItemHandleAccess::Create
author: windows-sdk-content
description: Creates a handle to a file.
old-location: winrt\istorageitemhandleaccess_create.htm
tech.root: WinRT
ms.assetid: 2BBF5CFE-0212-4133-BA19-DEA322ED5569
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Create, Create method [Windows Runtime], Create method [Windows Runtime],IStorageItemHandleAccess interface, IStorageItemHandleAccess interface [Windows Runtime],Create method, IStorageItemHandleAccess.Create, IStorageItemHandleAccess::Create, windowsstoragecom/IStorageItemHandleAccess::Create, winrt.istorageitemhandleaccess_create
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.storage.dll
api_name:
 - IStorageItemHandleAccess.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStorageItemHandleAccess::Create


## -description


Creates a handle to a file.


## -parameters




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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt765063(v=VS.85).aspx">IStorageItemHandleAccess</a>
 

 

