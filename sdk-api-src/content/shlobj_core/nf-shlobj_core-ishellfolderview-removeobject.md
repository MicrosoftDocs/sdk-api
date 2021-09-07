---
UID: NF:shlobj_core.IShellFolderView.RemoveObject
title: IShellFolderView::RemoveObject (shlobj_core.h)
description: RemoveObject may be altered or unavailable.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","RemoveObject method","IShellFolderView.RemoveObject","IShellFolderView::RemoveObject","RemoveObject","RemoveObject method [Windows Shell]","RemoveObject method [Windows Shell]","IShellFolderView interface","_shell_IShellFolderView_RemoveObject","shell.IShellFolderView_RemoveObject","shlobj_core/IShellFolderView::RemoveObject"]
old-location: shell\IShellFolderView_RemoveObject.htm
tech.root: shell
ms.assetid: 5e96040b-5b6a-4323-a5c4-f30e534ed15a
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],RemoveObject method, IShellFolderView.RemoveObject, IShellFolderView::RemoveObject, RemoveObject, RemoveObject method [Windows Shell], RemoveObject method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_RemoveObject, shell.IShellFolderView_RemoveObject, shlobj_core/IShellFolderView::RemoveObject
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
 - IShellFolderView::RemoveObject
 - shlobj_core/IShellFolderView::RemoveObject
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
 - IShellFolderView.RemoveObject
---

# IShellFolderView::RemoveObject


## -description

<p class="CCE_Message">[<b>RemoveObject</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes an item from the view.

## -parameters

### -param pidl [in, optional]

Type: <b>PUITEMID_CHILD</b>

A pointer to the item to remove from the view. This value can be <b>NULL</b>. When using the system folder view object (DefView) under Windows XP and Windows Vista, a <b>NULL</b> value results in the removal of all objects from the view.

### -param puItem [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the index position of the removed item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Items removed through this method can be readded to the view by the data source at any time.

