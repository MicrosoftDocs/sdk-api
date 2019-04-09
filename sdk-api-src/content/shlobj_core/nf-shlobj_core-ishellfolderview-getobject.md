---
UID: NF:shlobj_core.IShellFolderView.GetObject
title: IShellFolderView::GetObject (shlobj_core.h)
author: windows-sdk-content
description: Gets an item from the view.
old-location: shell\IShellFolderView_GetObject.htm
tech.root: shell
ms.assetid: a231e92f-b467-4fd7-929d-92259272a734
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [Windows Shell], GetObject method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetObject method, IShellFolderView.GetObject, IShellFolderView::GetObject, _shell_IShellFolderView_GetObject, shell.IShellFolderView_GetObject, shlobj_core/IShellFolderView::GetObject
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Shlobj_core.h
api_name:
 - IShellFolderView.GetObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::GetObject


## -description


<p class="CCE_Message">[<b>GetObject</b> is no longer available for use as of Windows Vista. Instead, use <a href="https://msdn.microsoft.com/c130ef36-1255-4c57-be31-7fc2029d9f66">IFolderView::Item</a>.]

Gets an item from the view.


## -parameters




### -param ppidl [out]

Type: <b>PITEMID_CHILD*</b>

When this method returns, contains the address of a pointer to the item at the given index.


### -param uItem

Type: <b>UINT</b>

The index of the item in the view to get.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



