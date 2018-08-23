---
UID: NF:shlobj_core.IShellFolderView.SetItemPos
title: IShellFolderView::SetItemPos
author: windows-sdk-content
description: Sets the position of the given item.
old-location: shell\IShellFolderView_SetItemPos.htm
old-project: shell
ms.assetid: d905260c-fa68-4b39-9c94-a74e1ac71b95
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellFolderView interface [Windows Shell],SetItemPos method, IShellFolderView.SetItemPos, IShellFolderView::SetItemPos, SetItemPos, SetItemPos method [Windows Shell], SetItemPos method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_SetItemPos, shell.IShellFolderView_SetItemPos, shlobj_core/IShellFolderView::SetItemPos
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.SetItemPos
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellFolderView::SetItemPos


## -description


<p class="CCE_Message">[This method has been deprecated. Use <a href="https://msdn.microsoft.com/1263bba8-63c8-4630-ab59-bb4ae10061fc">IFolderView::SelectAndPositionItems</a> instead.]

Sets the position of the given item.


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL that corresponds to the item for which the position is being set.


### -param ppt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a structure that contains the new coordinates of the item relative to the ListView contained in the view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



