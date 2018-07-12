---
UID: NF:shobjidl_core.IRelatedItem.GetItemIDList
title: IRelatedItem::GetItemIDList
author: windows-sdk-content
description: Gets the pointer to an item identifier list (PIDL) for the item that is related.
old-location: shell\IRelatedItem_GetItemIDList.htm
old-project: shell
ms.assetid: 2cef7dcb-be66-492c-a217-8b24d9f79506
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetItemIDList, GetItemIDList method [Windows Shell], GetItemIDList method [Windows Shell],IRelatedItem interface, IRelatedItem interface [Windows Shell],GetItemIDList method, IRelatedItem.GetItemIDList, IRelatedItem::GetItemIDList, _shell_IRelatedItem_GetItemIDList, shell.IRelatedItem_GetItemIDList, shobjidl_core/IRelatedItem::GetItemIDList
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
 - IRelatedItem.GetItemIDList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IRelatedItem::GetItemIDList


## -description


Gets the pointer to an item identifier list (PIDL) for the item that is related.


## -parameters




### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns, contains the PIDL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



