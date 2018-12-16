---
UID: NF:shlobj_core.IShellFolderView.IsDropOnSource
title: IShellFolderView::IsDropOnSource
author: windows-sdk-content
description: Checks whether the destination of the current drag-and-drop or cut-and-paste operation is the same as the source.
old-location: shell\IShellFolderView_IsDropOnSource.htm
tech.root: shell
ms.assetid: 3661fe68-b351-48e0-a098-8ad919bdfbb2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellFolderView interface [Windows Shell],IsDropOnSource method, IShellFolderView.IsDropOnSource, IShellFolderView::IsDropOnSource, IsDropOnSource, IsDropOnSource method [Windows Shell], IsDropOnSource method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_IsDropOnSource, shell.IShellFolderView_IsDropOnSource, shlobj_core/IShellFolderView::IsDropOnSource
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
 - shlobj_core.h
api_name:
 - IShellFolderView.IsDropOnSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::IsDropOnSource


## -description


<p class="CCE_Message">[This method has been deprecated. Use <a href="https://msdn.microsoft.com/1687a162-f81c-422b-afc2-0b5b8b6951ad">IFolderView2::IsMoveInSameFolder</a> instead.]

Checks whether the destination of the current drag-and-drop or cut-and-paste operation is the same as the source.


## -parameters




### -param pDropTarget [in, optional]

Type: <b><a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>*</b>

A pointer to a destination drop target object.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the destination is the same as the source.



