---
UID: NF:shlobj_core.IShellFolderView.SetCallback
title: IShellFolderView::SetCallback (shlobj_core.h)
author: windows-sdk-content
description: IShellFolderView::SetCallback may be altered or unavailable.
old-location: shell\IShellFolderView_SetCallback.htm
tech.root: shell
ms.assetid: 3438f4ba-e7f1-46b1-b85d-0e880615bb12
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],SetCallback method, IShellFolderView.SetCallback, IShellFolderView::SetCallback, SetCallback, SetCallback method [Windows Shell], SetCallback method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_SetCallback, shell.IShellFolderView_SetCallback, shlobj_core/IShellFolderView::SetCallback
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
 - IShellFolderView.SetCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellFolderView::SetCallback


## -description


<p class="CCE_Message">[<b>IShellFolderView::SetCallback</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Replaces the callback object used by the view.


## -parameters




### -param pNewCB [in, optional]

Type: <b><a href="https://msdn.microsoft.com/0cd2bce8-d77a-4140-869b-707aaa279796">IShellFolderViewCB</a>*</b>

A pointer to the new <a href="https://msdn.microsoft.com/0cd2bce8-d77a-4140-869b-707aaa279796">IShellFolderViewCB</a> callback object.


### -param ppOldCB [out, optional]

Type: <b><a href="https://msdn.microsoft.com/0cd2bce8-d77a-4140-869b-707aaa279796">IShellFolderViewCB</a>**</b>

The address of an interface pointer that, when this method returns successfully, points to the original <a href="https://msdn.microsoft.com/0cd2bce8-d77a-4140-869b-707aaa279796">IShellFolderViewCB</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



