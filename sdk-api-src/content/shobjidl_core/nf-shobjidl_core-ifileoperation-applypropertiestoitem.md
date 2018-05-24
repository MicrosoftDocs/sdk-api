---
UID: NF:shobjidl_core.IFileOperation.ApplyPropertiesToItem
title: IFileOperation::ApplyPropertiesToItem
author: windows-driver-content
description: Declares a single item whose property values are to be set.
old-location: shell\IFileOperation_ApplyPropertiesToItem.htm
old-project: shell
ms.assetid: 35330c7c-29fc-4337-a538-863925398b0d
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ApplyPropertiesToItem, ApplyPropertiesToItem method [Windows Shell], ApplyPropertiesToItem method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],ApplyPropertiesToItem method, IFileOperation.ApplyPropertiesToItem, IFileOperation::ApplyPropertiesToItem, _shell_IFileOperation_ApplyPropertiesToItem, shell.IFileOperation_ApplyPropertiesToItem, shobjidl_core/IFileOperation::ApplyPropertiesToItem
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileOperation.ApplyPropertiesToItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::ApplyPropertiesToItem


## -description


Declares a single item whose property values are to be set.


## -parameters




### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to the item to receive the new property values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not apply the properties to the item, it merely declares the item. To set property values on an item, you must make at least the sequence of calls detailed here:

                

<ol>
<li>Call <a href="https://msdn.microsoft.com/b54efc12-42e9-4a90-a4d9-0e75bcdba0d6">IFileOperation::SetProperties</a> to declare the specific properties to be set and their new values.</li>
<li>Call <b>IFileOperation::ApplyPropertiesToItem</b> to declare the item whose properties are to be set.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to apply the properties to the item.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/d24aa63e-99ef-470c-9723-e561ee0a56bc">IFileOperation::ApplyPropertiesToItems</a>
 

 

