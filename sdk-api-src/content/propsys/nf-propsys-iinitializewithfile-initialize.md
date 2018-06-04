---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IInitializeWithFile::Initialize


## -description


Initializes a handler with a file path.


## -parameters




### -param pszFilePath [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the file path as a null-terminated Unicode string.


### -param grfMode [in]

Type: <b>DWORD</b>

One of the following <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> values that indicates the access mode for <i>pszFilePath</i>.



#### STGM_READ

The file indicated by <b>IInitializeWithFile::Initialize</b> is read-only.



#### STGM_READWRITE

The file indicated by <b>IInitializeWithFile::Initialize</b> can be read from and written to.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> is preferred to this method because of its ability to use files that are not accessible through a Win32 path, such as the contents of a compressed file with a .zip file name extension. Use <b>IInitializeWithFile::Initialize</b> only when the API used by the handler to access the file accepts file paths only.

The file pointed to by <i>pszFilePath</i> must remain open for the lifetime of the handler or until <a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a> is called.

If the file cannot be opened according to the method's parameter values, this method returns a suitable error code.

A handler instance should be initialized only once in its lifetime. Attempts by the calling application to reinitialize the handler should result in the error <code>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</code>.



