---
UID: NF:shobjidl_core.IFolderView.ItemCount
title: IFolderView::ItemCount
author: windows-sdk-content
description: Gets the number of items in the folder. This can be the number of all items, or a subset such as the number of selected items.
old-location: shell\IFolderView_ItemCount.htm
tech.root: shell
ms.assetid: dadf91c5-7d27-4b1b-875b-6f0615440f47
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFolderView interface [Windows Shell],ItemCount method, IFolderView.ItemCount, IFolderView::ItemCount, ItemCount, ItemCount method [Windows Shell], ItemCount method [Windows Shell],IFolderView interface, _shell_IFolderView_ItemCount, shell.IFolderView_ItemCount, shobjidl_core/IFolderView::ItemCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderView.ItemCount
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
- IFolderView.ItemCount
: 
---

# IFolderView::ItemCount


## -description


Gets the number of items in the folder. This can be the number of all items, or a subset such as the number of selected items.


## -parameters




### -param uFlags [in]

Type: <b>UINT</b>

Flags from the <a href="https://msdn.microsoft.com/06ed616b-8121-4ea0-bd05-632888d0f376">_SVGIO</a> enumeration that limit the count to certain types of items.


### -param pcItems [out]

Type: <b>int*</b>

Pointer to an integer that receives the number of items (files and folders) displayed in the folder view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



