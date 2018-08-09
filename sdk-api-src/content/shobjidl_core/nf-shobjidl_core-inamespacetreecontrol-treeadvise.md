---
UID: NF:shobjidl_core.INameSpaceTreeControl.TreeAdvise
title: INameSpaceTreeControl::TreeAdvise
author: windows-sdk-content
description: Enables a client to register with the control.
old-location: shell\INameSpaceTreeControl_TreeAdvise.htm
old-project: shell
ms.assetid: d59b9772-7061-4ea5-964a-75deb293b407
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],TreeAdvise method, INameSpaceTreeControl.TreeAdvise, INameSpaceTreeControl::TreeAdvise, TreeAdvise, TreeAdvise method [Windows Shell], TreeAdvise method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_TreeAdvise, shell.INameSpaceTreeControl_TreeAdvise, shobjidl_core/INameSpaceTreeControl::TreeAdvise
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
 - INameSpaceTreeControl.TreeAdvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# INameSpaceTreeControl::TreeAdvise


## -description


Enables a client to register with the control.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the client IUnknown that registers with the control.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to the cookie that is passed back for registration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The pointer to the cookie that is passed back is used to unregister the control later with <a href="https://msdn.microsoft.com/9a0ba832-503a-48d6-80a7-7f6c51d60215">INameSpaceTreeControl::TreeUnadvise</a>.
            



