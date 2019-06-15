---
UID: NF:shobjidl_core.IFolderView.GetFolder
title: IFolderView::GetFolder (shobjidl_core.h)
author: windows-sdk-content
description: Gets the folder object.
old-location: shell\IFolderView_GetFolder.htm
tech.root: shell
ms.assetid: 4fdeb995-2220-4461-a4d6-80bce08153b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFolder, GetFolder method [Windows Shell], GetFolder method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetFolder method, IFolderView.GetFolder, IFolderView::GetFolder, _shell_IFolderView_GetFolder, shell.IFolderView_GetFolder, shobjidl_core/IFolderView::GetFolder
ms.topic: method
f1_keywords: ["shobjidl_core/IFolderView.GetFolder"]
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderView.GetFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderView::GetFolder


## -description


Gets the folder object.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID to represent the folder.


### -param ppv [out]

Type: <b>VOID**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> or a related interface. This can also be an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a> with a single element.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



