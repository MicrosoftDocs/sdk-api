---
UID: NF:shobjidl_core.IShellView2.HandleRename
title: IShellView2::HandleRename
author: windows-sdk-content
description: Used to change an item's identifier.
old-location: shell\IShellView2_HandleRename.htm
old-project: shell
ms.assetid: 0264df56-433f-4c54-a7e0-ccd92d3da602
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: HandleRename, HandleRename method [Windows Shell], HandleRename method [Windows Shell],IShellView2 interface, IShellView2 interface [Windows Shell],HandleRename method, IShellView2.HandleRename, IShellView2::HandleRename, _win32_IShellView2_HandleRename, shell.IShellView2_HandleRename, shobjidl_core/IShellView2::HandleRename
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellView2.HandleRename
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellView2::HandleRename


## -description


Used to change an item's identifier.


## -parameters




### -param pidlNew

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure. The current identifier is passed in and is replaced by the new one.


## -returns



Type: <b>HRESULT</b>

Return S_OK if successful, or a COM-defined error code otherwise.



