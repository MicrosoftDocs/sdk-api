---
UID: NF:shldisp.FolderItemVerbs.Item
title: FolderItemVerbs::Item
author: windows-sdk-content
description: Retrieves the FolderItemVerb object for a specified item in the collection.
old-location: shell\FolderItemVerbs_Item.htm
old-project: shell
ms.assetid: 65871926-0920-4ad6-82da-7aba0a3c0fab
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FolderItemVerbs object [Windows Shell],Item method, FolderItemVerbs.Item, FolderItemVerbs::Item, Item, Item method [Windows Shell], Item method [Windows Shell],FolderItemVerbs object, _win32_FolderItemVerbs_Item, shell.FolderItemVerbs_Item
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	FolderItemVerbs.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# FolderItemVerbs::Item


## -description


Retrieves the <a href="https://msdn.microsoft.com/22f52e3f-875e-4dde-8875-3228639bc7f1">FolderItemVerb</a> object for a specified item in the collection.


## -parameters




### -param index




### -param ppid






#### - iIndex [in]

Type: <b>Variant</b>

The zero-based index of the item to retrieve. This value must be less than the value of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a> property.


## -returns



Type: <b><a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>**</b>

Object that receives the <a href="https://msdn.microsoft.com/22f52e3f-875e-4dde-8875-3228639bc7f1">FolderItemVerb</a> object.



