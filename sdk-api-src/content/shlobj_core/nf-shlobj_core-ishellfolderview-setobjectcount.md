---
UID: NF:shlobj_core.IShellFolderView.SetObjectCount
title: IShellFolderView::SetObjectCount (shlobj_core.h)
description: SetObjectCount is no longer available.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","SetObjectCount method","IShellFolderView.SetObjectCount","IShellFolderView::SetObjectCount","SFVSOC_INVALIDATE_ALL","SFVSOC_NOSCROLL","SetObjectCount","SetObjectCount method [Windows Shell]","SetObjectCount method [Windows Shell]","IShellFolderView interface","_shell_IShellFolderView_SetObjectCount","shell.IShellFolderView_SetObjectCount","shlobj_core/IShellFolderView::SetObjectCount"]
old-location: shell\IShellFolderView_SetObjectCount.htm
tech.root: shell
ms.assetid: 0656fb51-1d10-42a5-bd4a-3ceb606c7176
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],SetObjectCount method, IShellFolderView.SetObjectCount, IShellFolderView::SetObjectCount, SFVSOC_INVALIDATE_ALL, SFVSOC_NOSCROLL, SetObjectCount, SetObjectCount method [Windows Shell], SetObjectCount method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_SetObjectCount, shell.IShellFolderView_SetObjectCount, shlobj_core/IShellFolderView::SetObjectCount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolderView::SetObjectCount
 - shlobj_core/IShellFolderView::SetObjectCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.SetObjectCount
---

# IShellFolderView::SetObjectCount


## -description

<p class="CCE_Message">[<b>SetObjectCount</b> is no longer available for use as of Windows Vista.]

Sets the number of items in the ListView control that the view contains.

## -parameters

### -param uCount

Type: <b>UINT</b>

The number of items to set the ListView control to.

### -param dwFlags

Type: <b>UINT</b>

Flags that control the behavior of the ListView control when the number of items is set. Includes the following:



#### SFVSOC_INVALIDATE_ALL (0x00000001)

The ListView control will not repaint unless affected items are currently in view. This is the default value.



#### SFVSOC_NOSCROLL (LVSICF_NOSCROLL)

The ListView control will not change the scroll position when the item count changes.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Starting with Windows Vista, calls to <b>SetObjectCount</b> always return E_NOTIMPL.

## -remarks

This method sends LVM_SETITEMCOUNT to the ListView control that the view contains, with WPARAM equal to <i>uCount</i> and LPARAM equal to <i>dwFlags</i>.

