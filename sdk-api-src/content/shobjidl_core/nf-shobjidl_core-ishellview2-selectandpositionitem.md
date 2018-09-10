---
UID: NF:shobjidl_core.IShellView2.SelectAndPositionItem
title: IShellView2::SelectAndPositionItem
author: windows-sdk-content
description: Selects and positions an item in a Shell View.
old-location: shell\IShellView2_SelectAndPositionItem.htm
tech.root: shell
ms.assetid: d78f152b-2dcb-410d-821a-56601a3c57f2
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IShellView2 interface [Windows Shell],SelectAndPositionItem method, IShellView2.SelectAndPositionItem, IShellView2::SelectAndPositionItem, SelectAndPositionItem, SelectAndPositionItem method [Windows Shell], SelectAndPositionItem method [Windows Shell],IShellView2 interface, _win32_IShellView2_SelectAndPositionItem, shell.IShellView2_SelectAndPositionItem, shobjidl_core/IShellView2::SelectAndPositionItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellView2.SelectAndPositionItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellView2::SelectAndPositionItem


## -description


Selects and positions an item in a Shell View.


## -parameters




### -param pidlItem

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that uniquely identifies the item of interest.


### -param uFlags

Type: <b>UINT</b>

One of the <a href="https://msdn.microsoft.com/3b0a7ec3-f365-48ec-86b0-ffd4c345deaf">_SVSIF</a> constants that specify the type of selection to apply.


### -param ppt

TBD




#### - point

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure containing the new position.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



