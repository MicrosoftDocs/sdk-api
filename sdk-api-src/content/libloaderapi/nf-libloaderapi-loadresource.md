---
UID: NF:libloaderapi.LoadResource
title: LoadResource function (libloaderapi.h)
description: Retrieves a handle that can be used to obtain a pointer to the first byte of the specified resource in memory.
old-location: menurc\loadresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\loadresource.htm
ms.date: 12/05/2018
ms.keywords: LoadResource, LoadResource function [Menus and Other Resources], _win32_LoadResource, _win32_loadresource_cpp, libloaderapi/LoadResource, menurc.loadresource, winui._win32_loadresource
ms.topic: function
f1_keywords:
- libloaderapi/LoadResource
dev_langs:
- c++
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
- LoadResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LoadResource function


## -description


Retrieves a handle that can be used to obtain a pointer to the first byte of the specified resource in memory.


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose executable file contains the resource. If <i>hModule</i> is <b>NULL</b>, the system loads the resource from the module that was used to create the current process.


### -param hResInfo [in]

Type: <b>HRSRC</b>

A handle to the resource to be loaded. This handle is returned by the <a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a> or <a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a> function.


## -returns



Type: <b>HGLOBAL</b>

If the function succeeds, the return value is a handle to the data associated with the resource.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The return type of <b>LoadResource</b> is <b>HGLOBAL</b> for backward compatibility, not because the function returns a handle to a global memory block. Do not pass this handle to the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function. To obtain a pointer to the first byte of the resource data, call the <a href="https://msdn.microsoft.com/a2385605-ad73-4250-ad78-36255144b816">LockResource</a> function; to obtain the size of the resource, call <a href="https://msdn.microsoft.com/e3eb82a3-15b6-4874-81d3-955d38d42383">SizeofResource</a>. 

To use a resource immediately, an application should use the following resource-specific functions to find and load the resource in one call.

<table class="clsStd">
<tr>
<th>Function</th>
<th>Action</th>
<th>To remove resource</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>
</td>
<td>Loads and formats a message-table entry</td>
<td>No action needed</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>
</td>
<td>Loads an accelerator table</td>
<td>
<a href="https://msdn.microsoft.com/17fd308f-c1ad-41aa-ae65-72e22a7500f3">DestroyAcceleratorTable</a>
</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadbitmapa">LoadBitmap</a>
</td>
<td>Loads a bitmap resource</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>
</td>
<td>Loads a cursor resource</td>
<td>
<a href="https://msdn.microsoft.com/fee6d837-9fc7-4ea6-b5d7-3889a64ccdea">DestroyCursor</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>
</td>
<td>Loads an icon resource</td>
<td>
<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/806297e1-0ee4-4471-a98a-598c1b48c0de">LoadMenu</a>
</td>
<td>Loads a menu resource</td>
<td>
<a href="https://msdn.microsoft.com/4fc9e332-09a6-4877-a831-e1128144530d">DestroyMenu</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9d878af7-a7b1-4d24-89ff-c567e4a8accd">LoadString</a>
</td>
<td>Loads a string resource</td>
<td>No action needed</td>
</tr>
</table>
 

For example, an application can use the <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a> function to load an icon for display on the screen, followed by <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> when done. 


#### Examples

For an example see <a href="https://docs.microsoft.com/windows-hardware/drivers/wdf/creating-a-resource-requirements-list">Updating Resources</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a>



<a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-loadmodule">LoadModule</a>



<a href="https://msdn.microsoft.com/a2385605-ad73-4250-ad78-36255144b816">LockResource</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

