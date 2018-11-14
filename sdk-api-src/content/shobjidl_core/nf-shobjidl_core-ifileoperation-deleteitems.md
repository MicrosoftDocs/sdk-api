---
UID: NF:shobjidl_core.IFileOperation.DeleteItems
title: IFileOperation::DeleteItems
author: windows-sdk-content
description: Declares a set of items that are to be deleted.
old-location: shell\IFileOperation_DeleteItems.htm
tech.root: shell
ms.assetid: 708072c4-c0c7-4d7d-a54f-234c57ff08e6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DeleteItems, DeleteItems method [Windows Shell], DeleteItems method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],DeleteItems method, IFileOperation.DeleteItems, IFileOperation::DeleteItems, _shell_IFileOperation_DeleteItems, shell.IFileOperation_DeleteItems, shobjidl_core/IFileOperation::DeleteItems
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
 - IFileOperation.DeleteItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IFileOperation.DeleteItems
: 
---

# IFileOperation::DeleteItems


## -description


Declares a set of items that are to be deleted.


## -parameters




### -param punkItems [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>, <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, or <a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a> object which represents the group of items to be deleted. You can also point to an <a href="https://msdn.microsoft.com/b367dc07-8a50-4562-bd73-57c73c781d81">IPersistIDList</a> object to represent a single item, effectively accomplishing the same function as <a href="https://msdn.microsoft.com/177ce480-0309-4ec8-a6f2-0be9196bd2c8">IFileOperation::DeleteItem</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not delete the items, it merely declares the items to be deleted. To delete a group of items, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::DeleteItems</b> to declare the files or folders to be deleted.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to begin the delete operation.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/177ce480-0309-4ec8-a6f2-0be9196bd2c8">IFileOperation::DeleteItem</a>
 

 

