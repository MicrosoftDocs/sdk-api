---
UID: NF:libloaderapi.LockResource
title: LockResource function (libloaderapi.h)
author: windows-sdk-content
description: Retrieves a pointer to the specified resource in memory.
old-location: menurc\lockresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\lockresource.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LockResource, LockResource function [Menus and Other Resources], _win32_LockResource, _win32_lockresource_cpp, libloaderapi/LockResource, menurc.lockresource, winui._win32_lockresource
ms.topic: function
f1_keywords: ["libloaderapi/LockResource"]
req.header: libloaderapi.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - LockResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LockResource function


## -description


Retrieves a pointer to the specified resource in memory.


## -parameters




### -param hResData [in]

Type: <b>HGLOBAL</b>

A handle to the resource to be accessed. The <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a> function returns this handle. Note that this parameter is listed as an <b>HGLOBAL</b> variable only for backward compatibility. Do not pass any value as a parameter other than a successful return value from the <b>LoadResource</b> function.


## -returns



Type: <b>LPVOID</b>

If the loaded resource is available, the return value is a pointer to the first byte of the resource; otherwise, it is <b>NULL</b>.




## -remarks



The pointer returned by <b>LockResource</b> is valid until the module containing the resource is unloaded. It is not necessary to unlock resources because the system automatically deletes them when the process that created them terminates.

Do not try to lock a resource by using the handle returned by the <a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a> or <a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a> function. Such a handle points to random data. 

<div class="alert"><b>Note</b>  <b>LockResource</b> does not actually lock memory; it is just used to obtain a pointer to 

the memory containing the resource data. The name of the function comes from versions prior to Windows XP, when it was 

used to lock a global memory block allocated by <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a>.</div>
<div> </div>

#### Examples

For an example, see <a href="https://docs.microsoft.com/windows-hardware/drivers/wdf/creating-a-resource-requirements-list">Updating Resources</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a>



<a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a>



<a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

