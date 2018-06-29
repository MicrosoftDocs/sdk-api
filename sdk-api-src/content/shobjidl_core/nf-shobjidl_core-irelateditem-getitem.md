---
UID: NF:shobjidl_core.IRelatedItem.GetItem
title: IRelatedItem::GetItem
author: windows-sdk-content
description: Gets the IShellItem that is related to this item.
old-location: shell\IRelatedItem_GetItem.htm
old-project: shell
ms.assetid: 4aaf0016-1a0d-49ef-a001-bc4a7fe90758
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetItem, GetItem method [Windows Shell], GetItem method [Windows Shell],IRelatedItem interface, IRelatedItem interface [Windows Shell],GetItem method, IRelatedItem.GetItem, IRelatedItem::GetItem, _shell_IRelatedItem_GetItem, shell.IRelatedItem_GetItem, shobjidl_core/IRelatedItem::GetItem
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
 - IRelatedItem.GetItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IRelatedItem::GetItem


## -description


Gets the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that is related to this item.


## -parameters




### -param ppsi

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

When this method returns, contains the address of a pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interface for the item that is related to this item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



