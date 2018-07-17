---
UID: NF:windowsstoragecom.IStorageFolderHandleAccess.Create
title: IStorageFolderHandleAccess::Create
author: windows-sdk-content
description: Creates a handle to a file that is in a storage folder.
old-location: winrt\istoragefolderhandleaccess_create.htm
old-project: WinRT
ms.assetid: CAA79CEC-FB04-48F0-BCF8-19613FA6D108
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Create, Create method [Windows Runtime], Create method [Windows Runtime],IStorageFolderHandleAccess interface, IStorageFolderHandleAccess interface [Windows Runtime],Create method, IStorageFolderHandleAccess.Create, IStorageFolderHandleAccess::Create, windowsstoragecom/IStorageFolderHandleAccess::Create, winrt.istoragefolderhandleaccess_create
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.storage.dll
api_name:
 - IStorageFolderHandleAccess.Create
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.storage.dll
req.irql: 
req.product: Windows Address Book 5.0
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C579B4D9-0CD6-45D7-BE6D-54FDFB3E7753">IStorageFolderHandleAccess</a>
 

 

