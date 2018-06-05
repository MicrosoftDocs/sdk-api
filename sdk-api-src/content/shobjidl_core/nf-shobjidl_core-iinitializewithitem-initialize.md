---
UID: NF:shobjidl_core.IInitializeWithItem.Initialize
title: IInitializeWithItem::Initialize
author: windows-sdk-content
description: Initializes a handler with an IShellItem.
old-location: shell\IInitializeWithItem_Initialize.htm
old-project: shell
ms.assetid: 61abf5c8-2847-4788-9d99-65f3b1c821d6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IInitializeWithItem interface [Windows Shell],Initialize method, IInitializeWithItem.Initialize, IInitializeWithItem::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithItem interface, STGM_READ, STGM_READWRITE, shell.IInitializeWithItem_Initialize, shell_IInitializeWithItem_Initialize, shobjidl_core/IInitializeWithItem::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Propsys.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
-	IInitializeWithItem.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IInitializeWithItem::Initialize


## -description


Initializes a handler with an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


### -param grfMode [in]

Type: <b>DWORD</b>

One of the following <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> values that indicate the access mode for <i>psi</i>.



#### STGM_READ

The <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> is read-only.



#### STGM_READWRITE

The <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> is read/write accessible.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> cannot be accessed, this method returns an appropriate error code.

A handler instance should be initialized only once in its lifetime. Attempts by the calling application to reinitialize the handler result in the error <code>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</code>.



