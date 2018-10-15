---
UID: NF:shobjidl_core.IFileOperation.RenameItems
title: IFileOperation::RenameItems
author: windows-sdk-content
description: Declares a set of items that are to be given a new display name. All items are given the same name.
old-location: shell\IFileOperation_RenameItems.htm
tech.root: shell
ms.assetid: 325c09c6-ae32-4f5d-8b21-174dafc94aea
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IFileOperation interface [Windows Shell],RenameItems method, IFileOperation.RenameItems, IFileOperation::RenameItems, RenameItems, RenameItems method [Windows Shell], RenameItems method [Windows Shell],IFileOperation interface, _shell_IFileOperation_RenameItems, shell.IFileOperation_RenameItems, shobjidl_core/IFileOperation::RenameItems
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
 - IFileOperation.RenameItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperation::RenameItems


## -description


Declares a set of items that are to be given a new display name. All items are given the same name.


## -parameters




### -param pUnkItems [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>, <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, or <a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a> object which represents the group of items to be renamed. You can also point to an <a href="https://msdn.microsoft.com/b367dc07-8a50-4562-bd73-57c73c781d81">IPersistIDList</a> object to represent a single item, effectively accomplishing the same function as <a href="https://msdn.microsoft.com/2f72b729-3535-4ab7-9579-21b1ba97c67f">IFileOperation::RenameItem</a>.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the new display name of the items. This is a null-terminated, Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If more than one of the items in the collection at <i>pUnkItems</i> is in the same folder, the renamed files are appended with a number in parentheses to differentiate them, for instance newfile(1).txt, newfile(2).txt, and newfile(3).txt.

This method does not rename the items, it merely declares the items to be renamed. To rename a group of objects, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::RenameItems</b> to declare the source files or folders and the new name.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to begin the rename operation.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/2f72b729-3535-4ab7-9579-21b1ba97c67f">IFileOperation::RenameItem</a>
 

 

