---
UID: NF:shlobj.IShellImageStore.Close
title: IShellImageStore::Close
author: windows-sdk-content
description: Closes the image cache.
old-location: shell\IShellImageStore_Close.htm
tech.root: shell
ms.assetid: 6228228a-1c12-467c-849c-b360d79ee5ca
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Close, Close method [Windows Shell], Close method [Windows Shell],IShellImageStore interface, IShellImageStore interface [Windows Shell],Close method, IShellImageStore.Close, IShellImageStore::Close, _win32_IShellImageStore_Close, shell.IShellImageStore_Close, shlobj/IShellImageStore::Close
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageStore.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageStore::Close


## -description


Closes the image cache.


## -parameters




### -param pdwLock

TBD




#### - pdwLoc [in]

Type: <b>const DWORD*</b>

A pointer to a variable of type <b>DWORD</b> that specifies the address that receives the lock during the call to the <a href="https://msdn.microsoft.com/2aebf791-7681-42b3-8ffe-46e103e7c036">IShellImageStore::Open</a> method.


## -returns



Type: <b>HRESULT</b>

Returns S_FALSE if the store is not open or if the store cannot be saved. Returns the result of <a href="https://msdn.microsoft.com/99ae5347-b140-4698-9fc5-bd60870d9149">IShellImageStore::Commit</a> otherwise.




## -remarks



<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/746bd660-17b6-4669-8f23-254f5d7dde82">IShellImageStore</a> is supported through Windows XP. It is not supported in later operating systems.</div>
<div> </div>


