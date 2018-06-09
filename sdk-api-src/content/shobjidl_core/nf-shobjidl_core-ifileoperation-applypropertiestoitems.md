---
UID: NF:shobjidl_core.IFileOperation.ApplyPropertiesToItems
title: IFileOperation::ApplyPropertiesToItems
author: windows-sdk-content
description: Declares a set of items for which to apply a common set of property values.
old-location: shell\IFileOperation_ApplyPropertiesToItems.htm
old-project: shell
ms.assetid: d24aa63e-99ef-470c-9723-e561ee0a56bc
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ApplyPropertiesToItems, ApplyPropertiesToItems method [Windows Shell], ApplyPropertiesToItems method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],ApplyPropertiesToItems method, IFileOperation.ApplyPropertiesToItems, IFileOperation::ApplyPropertiesToItems, _shell_IFileOperation_ApplyPropertiesToItems, shell.IFileOperation_ApplyPropertiesToItems, shobjidl_core/IFileOperation::ApplyPropertiesToItems
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
 - IFileOperation.ApplyPropertiesToItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::ApplyPropertiesToItems


## -description


Declares a set of items for which to apply a common set of property values.


## -parameters




### -param punkItems [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>, <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, or <a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a> object which represents the group of items.  You can also point to an <a href="https://msdn.microsoft.com/b367dc07-8a50-4562-bd73-57c73c781d81">IPersistIDList</a> object to represent a single item, effectively accomplishing the same function as <a href="https://msdn.microsoft.com/35330c7c-29fc-4337-a538-863925398b0d">IFileOperation::ApplyPropertiesToItem</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not apply the properties to the items, it merely declares the items. To set property values on a group of items, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <a href="https://msdn.microsoft.com/b54efc12-42e9-4a90-a4d9-0e75bcdba0d6">IFileOperation::SetProperties</a> to declare the specific properties to be set and their new values.</li>
<li>Call <b>IFileOperation::ApplyPropertiesToItems</b> to declare the items whose property values are to be set.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to apply the properties to the items.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/35330c7c-29fc-4337-a538-863925398b0d">IFileOperation::ApplyPropertiesToItem</a>
 

 

