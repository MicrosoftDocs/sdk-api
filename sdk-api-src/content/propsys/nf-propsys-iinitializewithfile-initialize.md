---
UID: NF:propsys.IInitializeWithFile.Initialize
title: IInitializeWithFile::Initialize (propsys.h)
author: windows-sdk-content
description: Initializes a handler with a file path.
old-location: shell\IInitializeWithFile_Initialize.htm
tech.root: shell
ms.assetid: 7b7bb534-dff7-455b-baee-f573fb645cc3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInitializeWithFile interface [Windows Shell],Initialize method, IInitializeWithFile.Initialize, IInitializeWithFile::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithFile interface, STGM_READ, STGM_READWRITE, propsys/IInitializeWithFile::Initialize, shell.IInitializeWithFile_Initialize, shell_IInitializeWithFile_Initialize
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IInitializeWithFile.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://msdn.microsoft.com/1e04c0a4-aa9b-4e2c-8307-525809ca903f">Initialize</a> is preferred to this method because of its ability to use files that are not accessible through a Win32 path, such as the contents of a compressed file with a .zip file name extension. Use <b>IInitializeWithFile::Initialize</b> only when the API used by the handler to access the file accepts file paths only.

The file pointed to by <i>pszFilePath</i> must remain open for the lifetime of the handler or until <a href="https://msdn.microsoft.com/25b6913e-e630-4cae-b155-d9d475593c9e">IPropertyStore::Commit</a> is called.

If the file cannot be opened according to the method's parameter values, this method returns a suitable error code.

A handler instance should be initialized only once in its lifetime. Attempts by the calling application to reinitialize the handler should result in the error <code>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</code>.



