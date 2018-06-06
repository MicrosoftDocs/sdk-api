---
UID: NF:shlobj_core.ILIsEqual
title: ILIsEqual function
author: windows-sdk-content
description: Tests whether two ITEMIDLIST structures are equal in a binary comparison.
old-location: shell\ILIsEqual.htm
old-project: shell
ms.assetid: 139613fc-cd3b-4d5b-b590-096af8f01b62
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ILIsEqual, ILIsEqual function [Windows Shell], _win32_ILIsEqual, shell.ILIsEqual, shlobj_core/ILIsEqual
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - Windows.Storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - ILIsEqual
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# ILIsEqual function


## -description


Tests whether two <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures are equal in a binary comparison.


## -parameters




### -param pidl1 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The first <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


### -param pidl2 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The second <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the two structures are equal, <b>FALSE</b> otherwise.




## -remarks



<b>ILIsEqual</b> performs a binary comparison of the item data. It is possible for two <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures to differ at the binary level while referring to the same item. <a href="https://msdn.microsoft.com/54d805cc-5396-4892-9347-cafc2d90779f">IShellFolder::CompareIDs</a> should be used to perform a non-binary comparison.



