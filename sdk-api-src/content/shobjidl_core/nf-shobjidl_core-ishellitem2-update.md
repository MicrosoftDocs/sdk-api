---
UID: NF:shobjidl_core.IShellItem2.Update
title: IShellItem2::Update
author: windows-sdk-content
description: Ensures that any cached information in this item is updated.
old-location: shell\IShellItem2_Update.htm
old-project: shell
ms.assetid: 42000a83-2ee0-49b9-b3fc-328685e25c0b
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IShellItem2 interface [Windows Shell],Update method, IShellItem2.Update, IShellItem2::Update, Update, Update method [Windows Shell], Update method [Windows Shell],IShellItem2 interface, _shell_IShellItem2_Update, shell.IShellItem2_Update, shobjidl_core/IShellItem2::Update
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
 - IShellItem2.Update
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItem2::Update


## -description


Ensures that any cached information in this item is updated.


## -parameters




### -param pbc [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on a bind context object.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including ERROR_FILE_NOT_FOUND if the item does not exist.



