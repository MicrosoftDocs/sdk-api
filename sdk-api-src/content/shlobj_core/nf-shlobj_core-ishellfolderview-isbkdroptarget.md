---
UID: NF:shlobj_core.IShellFolderView.IsBkDropTarget
title: IShellFolderView::IsBkDropTarget
author: windows-sdk-content
description: IsBkDropTarget may be altered or unavailable.
old-location: shell\IShellFolderView_IsBkDropTarget.htm
tech.root: shell
ms.assetid: 6de58057-2bcd-480e-8b4a-6e59aad168dc
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IShellFolderView interface [Windows Shell],IsBkDropTarget method, IShellFolderView.IsBkDropTarget, IShellFolderView::IsBkDropTarget, IsBkDropTarget, IsBkDropTarget method [Windows Shell], IsBkDropTarget method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_IsBkDropTarget, shell.IShellFolderView_IsBkDropTarget, shlobj_core/IShellFolderView::IsBkDropTarget
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IShellFolderView.IsBkDropTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::IsBkDropTarget


## -description


<p class="CCE_Message">[<b>IsBkDropTarget</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Checks if the target of a drag-and-drop operation is the background of the view.


## -parameters




### -param pDropTarget [in, optional]

Type: <b><a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>*</b>

A pointer to the target of the drag-and-drop operation.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the target of the drag-and-drop operation is to the background of the view, S_FALSE otherwise.



