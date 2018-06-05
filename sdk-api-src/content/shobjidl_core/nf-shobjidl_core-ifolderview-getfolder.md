---
UID: NF:shobjidl_core.IFolderView.GetFolder
title: IFolderView::GetFolder
author: windows-sdk-content
description: Gets the folder object.
old-location: shell\IFolderView_GetFolder.htm
old-project: shell
ms.assetid: 4fdeb995-2220-4461-a4d6-80bce08153b1
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetFolder, GetFolder method [Windows Shell], GetFolder method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetFolder method, IFolderView.GetFolder, IFolderView::GetFolder, _shell_IFolderView_GetFolder, shell.IFolderView_GetFolder, shobjidl_core/IFolderView::GetFolder
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IFolderView.GetFolder
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
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

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> or a related interface. This can also be an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a> with a single element.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



