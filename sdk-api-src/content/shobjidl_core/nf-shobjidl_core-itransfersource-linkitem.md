---
UID: NF:shobjidl_core.ITransferSource.LinkItem
title: ITransferSource::LinkItem
author: windows-sdk-content
description: Not implemented.
old-location: shell\ITransferSource_LinkItem.htm
tech.root: shell
ms.assetid: e373c790-5366-4bff-a08d-817b0c566b1d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITransferSource interface [Windows Shell],LinkItem method, ITransferSource.LinkItem, ITransferSource::LinkItem, LinkItem, LinkItem method [Windows Shell], LinkItem method [Windows Shell],ITransferSource interface, _shell_ITransferSource_LinkItem, shell.ITransferSource_LinkItem, shobjidl_core/ITransferSource::LinkItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ITransferSource.LinkItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- ITransferSource.LinkItem
: 
---

# ITransferSource::LinkItem


## -description


Not implemented.


## -parameters




### -param psiSource [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the source item.


### -param psiParentDest [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> as parent to link.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string containing the name for the link.


### -param flags [in]

Type: <b>DWORD</b>

The flags that control the file operation. Value is one or more of the <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> constants.


### -param ppsiNewDest [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

When the method returns, contains the address of a pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> of the link.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



