---
UID: NF:shobjidl_core.IShellItemFilter.GetEnumFlagsForItem
title: IShellItemFilter::GetEnumFlagsForItem
author: windows-sdk-content
description: Allows a client to specify which classes of objects in a Shell item should be enumerated for inclusion in the view.
old-location: shell\IShellItemFilter_GetEnumFlagsForItem.htm
old-project: shell
ms.assetid: a84868ab-25c4-4cb7-84a1-aba0eff09b4a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetEnumFlagsForItem, GetEnumFlagsForItem method [Windows Shell], GetEnumFlagsForItem method [Windows Shell],IShellItemFilter interface, IShellItemFilter interface [Windows Shell],GetEnumFlagsForItem method, IShellItemFilter.GetEnumFlagsForItem, IShellItemFilter::GetEnumFlagsForItem, _shell_IShellItemFilter_GetEnumFlagsForItem, shell.IShellItemFilter_GetEnumFlagsForItem, shobjidl_core/IShellItemFilter::GetEnumFlagsForItem
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
 - IShellItemFilter.GetEnumFlagsForItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItemFilter::GetEnumFlagsForItem


## -description


Allows a client to specify which classes of objects in a <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">Shell item</a> should be enumerated for inclusion in the view.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">Shell item</a> for which the <a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a> enum flags are to be retrieved.


### -param pgrfFlags [out]

Type: <b><a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a> enum flags for the given <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">Shell item</a> that specifies which classes of objects to enumerate for inclusion in the view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>



<a href="https://msdn.microsoft.com/c2873385-a25d-4d9d-94ef-05dcdf284be1">IShellItemFilter</a>



<a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a>
 

 

