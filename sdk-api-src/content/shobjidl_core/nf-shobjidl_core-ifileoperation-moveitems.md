---
UID: NF:shobjidl_core.IFileOperation.MoveItems
title: IFileOperation::MoveItems
author: windows-sdk-content
description: Declares a set of items that are to be moved to a specified destination.
old-location: shell\IFileOperation_MoveItems.htm
old-project: shell
ms.assetid: 7b3c3fc9-5e08-44be-b0ba-a67702e2deb6
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IFileOperation interface [Windows Shell],MoveItems method, IFileOperation.MoveItems, IFileOperation::MoveItems, MoveItems, MoveItems method [Windows Shell], MoveItems method [Windows Shell],IFileOperation interface, _shell_IFileOperation_MoveItems, shell.IFileOperation_MoveItems, shobjidl_core/IFileOperation::MoveItems
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperation.MoveItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::MoveItems


## -description


Declares a set of items that are to be moved to a specified destination.


## -parameters




### -param punkItems [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>, <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, or <a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a> object which represents the group of items to be moved. You can also point to an <a href="https://msdn.microsoft.com/b367dc07-8a50-4562-bd73-57c73c781d81">IPersistIDList</a> object to represent a single item, effectively accomplishing the same function as <a href="https://msdn.microsoft.com/7b1e66c9-5264-42cb-9554-d1ea92625c6f">IFileOperation::MoveItem</a>.


### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder to contain the moved items.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not move the items, it merely declares the items to be moved. To move a group of items, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::MoveItems</b> to declare the source files or folders and the destination folder.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to begin the move operation.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/7b1e66c9-5264-42cb-9554-d1ea92625c6f">IFileOperation::MoveItem</a>
 

 

