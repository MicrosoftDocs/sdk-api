---
UID: NF:shobjidl.IResultsFolder.RemoveItem
title: IResultsFolder::RemoveItem
author: windows-driver-content
description: Removes an item from a results folder.
old-location: shell\IResultsFolder_RemoveItem.htm
old-project: shell
ms.assetid: 17be32ed-50d7-4c16-9a06-97c4a0f8dc8d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IResultsFolder interface [Windows Shell],RemoveItem method, IResultsFolder.RemoveItem, IResultsFolder::RemoveItem, RemoveItem, RemoveItem method [Windows Shell], RemoveItem method [Windows Shell],IResultsFolder interface, _shell_IResultsFolder_RemoveItem, shell.IResultsFolder_RemoveItem, shobjidl/IResultsFolder::RemoveItem
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	IResultsFolder.RemoveItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IResultsFolder::RemoveItem


## -description


Removes an item from a results folder.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



