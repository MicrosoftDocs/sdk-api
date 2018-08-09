---
UID: NF:shobjidl_core.INameSpaceTreeControl.RemoveRoot
title: INameSpaceTreeControl::RemoveRoot
author: windows-sdk-content
description: Removes a root and its children from a tree.
old-location: shell\INameSpaceTreeControl_RemoveRoot.htm
old-project: shell
ms.assetid: e27e4eca-60f3-47b7-95cd-c004cda78d77
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],RemoveRoot method, INameSpaceTreeControl.RemoveRoot, INameSpaceTreeControl::RemoveRoot, RemoveRoot, RemoveRoot method [Windows Shell], RemoveRoot method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_RemoveRoot, shell.INameSpaceTreeControl_RemoveRoot, shobjidl_core/INameSpaceTreeControl::RemoveRoot
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl.RemoveRoot
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# INameSpaceTreeControl::RemoveRoot


## -description


Removes a root and its children from a tree.


## -parameters




### -param psiRoot [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the root that is to be removed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



