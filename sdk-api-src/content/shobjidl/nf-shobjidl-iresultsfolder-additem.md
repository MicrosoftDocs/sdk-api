---
UID: NF:shobjidl.IResultsFolder.AddItem
title: IResultsFolder::AddItem
author: windows-sdk-content
description: Adds an item to a results folder.
old-location: shell\IResultsFolder_AddItem.htm
tech.root: shell
ms.assetid: 005f7125-8dc2-4d9c-a860-1bb56b4d0b63
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: AddItem, AddItem method [Windows Shell], AddItem method [Windows Shell],IResultsFolder interface, IResultsFolder interface [Windows Shell],AddItem method, IResultsFolder.AddItem, IResultsFolder::AddItem, _shell_IResultsFolder_AddItem, shell.IResultsFolder_AddItem, shobjidl/IResultsFolder::AddItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
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
 - Shobjidl.h
api_name:
 - IResultsFolder.AddItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResultsFolder::AddItem


## -description


Adds an item to a results folder.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



