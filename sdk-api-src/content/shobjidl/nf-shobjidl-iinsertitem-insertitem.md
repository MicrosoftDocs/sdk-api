---
UID: NF:shobjidl.IInsertItem.InsertItem
title: IInsertItem::InsertItem
author: windows-sdk-content
description: Adds an ITEMIDLIST structure to a list of such structures.
old-location: shell\IInsertitem_InsertItem.htm
tech.root: shell
ms.assetid: 45a25357-9bb1-4298-9ffb-20081e3072a5
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IInsertItem interface [Windows Shell],InsertItem method, IInsertItem.InsertItem, IInsertItem::InsertItem, InsertItem, InsertItem method [Windows Shell], InsertItem method [Windows Shell],IInsertItem interface, shell.IInsertitem_InsertItem, shell_IInsertitem_InsertItem, shobjidl/IInsertItem::InsertItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IInsertItem.InsertItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInsertItem::InsertItem


## -description


Adds an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure to a list of such structures.


## -parameters




### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that corresponds to an item in a Shell folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



