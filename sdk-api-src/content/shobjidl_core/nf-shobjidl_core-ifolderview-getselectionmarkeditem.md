---
UID: NF:shobjidl_core.IFolderView.GetSelectionMarkedItem
title: IFolderView::GetSelectionMarkedItem
author: windows-driver-content
description: Gets the index of an item in the folder's view which has been marked by using the SVSI_SELECTIONMARK in IFolderView::SelectItem.
old-location: shell\IFolderView_GetSelectionMarkedItem.htm
old-project: shell
ms.assetid: 86416704-c2e3-4782-a566-b49cbd0e7696
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetSelectionMarkedItem, GetSelectionMarkedItem method [Windows Shell], GetSelectionMarkedItem method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetSelectionMarkedItem method, IFolderView.GetSelectionMarkedItem, IFolderView::GetSelectionMarkedItem, _shell_IFolderView_GetSelectionMarkedItem, shell.IFolderView_GetSelectionMarkedItem, shobjidl_core/IFolderView::GetSelectionMarkedItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	Shell32.dll
api_name:
-	IFolderView.GetSelectionMarkedItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderView::GetSelectionMarkedItem


## -description


Gets the index of an item in the folder's view which has been marked by using the SVSI_SELECTIONMARK in <a href="https://msdn.microsoft.com/6db262ea-861b-4bc5-955f-b81945313ea8">IFolderView::SelectItem</a>.


## -parameters




### -param piItem [out]

Type: <b>int*</b>

A pointer to the index of the marked item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/6db262ea-861b-4bc5-955f-b81945313ea8">IFolderView::SelectItem</a>
 

 

