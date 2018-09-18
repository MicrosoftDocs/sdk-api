---
UID: NF:shobjidl_core.IFileOperationProgressSink.PostNewItem
title: IFileOperationProgressSink::PostNewItem
author: windows-sdk-content
description: Performs caller-implemented actions after the new item is created.
old-location: shell\IFileOperationProgressSink_PostNewItem.htm
tech.root: shell
ms.assetid: 250ca9b8-951d-4ce8-bfb7-d512f4a59a39
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PostNewItem method, IFileOperationProgressSink.PostNewItem, IFileOperationProgressSink::PostNewItem, PostNewItem, PostNewItem method [Windows Shell], PostNewItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PostNewItem, shell.IFileOperationProgressSink_PostNewItem, shobjidl_core/IFileOperationProgressSink::PostNewItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IFileOperationProgressSink.PostNewItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperationProgressSink::PostNewItem


## -description


Performs caller-implemented actions after the new item is created.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that were used during the creation operation. Some values can be set or changed during the creation operation. See <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.


### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder to which the new item was added.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the file name of the new item, for instance <b>Newfile.txt</b>. This is a null-terminated, Unicode string.


### -param pszTemplateName [in]

Type: <b>LPCWSTR</b>

Pointer to the name of the template file (for example <b>Excel9.xls</b>) that the new item is based on, stored in one of the following locations:
                    
                    

<ul>
<li>CSIDL_COMMON_TEMPLATES. The default path for this folder is %ALLUSERSPROFILE%\Templates.</li>
<li>CSIDL_TEMPLATES. The default path for this folder is %USERPROFILE%\Templates.</li>
<li>%SystemRoot%\shellnew</li>
</ul>
This is a null-terminated, Unicode string used to specify an existing file of the same type as the new file, containing the minimal content that an application wants to include in any new file.

This parameter is normally <b>NULL</b> to specify a new, blank file.


### -param dwFileAttributes [in]

Type: <b>DWORD</b>

The file attributes applied to the new item. One or more of the values found at <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>.


### -param hrNew [in]

Type: <b>HRESULT</b>

The return value of the creation operation. Note that this is not the HRESULT returned by <a href="https://msdn.microsoft.com/810a1275-cae2-4487-b517-22aa8e4374a9">NewItem</a>, which simply queues the creation operation. Instead, this is the result of the actual creation.


### -param psiNewItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the new item.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, all subsequent operations pending from the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> are canceled.



