---
UID: NF:shobjidl_core.INameSpaceTreeControl.TreeUnadvise
title: INameSpaceTreeControl::TreeUnadvise
author: windows-sdk-content
description: Enables a client to unregister with the control.
old-location: shell\INameSpaceTreeControl_TreeUnadvise.htm
old-project: shell
ms.assetid: 9a0ba832-503a-48d6-80a7-7f6c51d60215
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],TreeUnadvise method, INameSpaceTreeControl.TreeUnadvise, INameSpaceTreeControl::TreeUnadvise, TreeUnadvise, TreeUnadvise method [Windows Shell], TreeUnadvise method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_TreeUnadvise, shell.INameSpaceTreeControl_TreeUnadvise, shobjidl_core/INameSpaceTreeControl::TreeUnadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	shobjidl_core.h
api_name:
-	INameSpaceTreeControl.TreeUnadvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# INameSpaceTreeControl::TreeUnadvise


## -description


Enables a client to unregister with the control.


## -parameters




### -param dwCookie






#### - pdwCookie [in]

Type: <b>DWORD*</b>

A pointer to the cookie that is to be unregistered.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The pointer to the cookie that is passed in is the one that was passed back in <a href="https://msdn.microsoft.com/d59b9772-7061-4ea5-964a-75deb293b407">INameSpaceTreeControl::TreeAdvise</a>.
            



