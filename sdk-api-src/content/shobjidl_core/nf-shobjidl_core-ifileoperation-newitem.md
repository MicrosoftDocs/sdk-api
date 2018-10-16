---
UID: NF:shobjidl_core.IFileOperation.NewItem
title: IFileOperation::NewItem
author: windows-sdk-content
description: Declares a new item that is to be created in a specified location.
old-location: shell\IFileOperation_NewItem.htm
tech.root: shell
ms.assetid: 810a1275-cae2-4487-b517-22aa8e4374a9
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IFileOperation interface [Windows Shell],NewItem method, IFileOperation.NewItem, IFileOperation::NewItem, NewItem, NewItem method [Windows Shell], NewItem method [Windows Shell],IFileOperation interface, _shell_IFileOperation_NewItem, shell.IFileOperation_NewItem, shobjidl_core/IFileOperation::NewItem
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
 - IFileOperation.NewItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperation::NewItem


## -description


Declares a new item that is to be created in a specified location.


## -parameters




### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder that will contain the new item.


### -param dwFileAttributes [in]

Type: <b>DWORD</b>

A bitwise value that specifies the file system attributes for the file or folder. See <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a> for possible values.


### -param pszName [in]

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


### -param pfopsItem [in]

Type: <b><a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a> object to be used for status and failure notifications. If you call <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the creation operation are included there, so set this parameter to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not create the new item, it merely declares the item to be created. To create a new item, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::NewItem</b> to declare the specifics of the new file or folder.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to create the new item.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/250ca9b8-951d-4ce8-bfb7-d512f4a59a39">PostNewItem</a>



<a href="https://msdn.microsoft.com/ea6223e1-a574-4e4b-a264-384f33579c6d">PreNewItem</a>
 

 

