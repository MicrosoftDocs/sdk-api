---
UID: NF:shobjidl_core.SHCreateShellItemArrayFromIDLists
title: SHCreateShellItemArrayFromIDLists function
author: windows-sdk-content
description: Creates a Shell item array object from a list of ITEMIDLIST structures.
old-location: shell\SHCreateShellItemArrayFromIDLists.htm
old-project: shell
ms.assetid: af462941-8c23-4f48-baf5-1ead9739a2c5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHCreateShellItemArrayFromIDLists, SHCreateShellItemArrayFromIDLists function [Windows Shell], _shell_SHCreateShellItemArrayFromIDLists, shell.SHCreateShellItemArrayFromIDLists, shobjidl_core/SHCreateShellItemArrayFromIDLists
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHCreateShellItemArrayFromIDLists
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHCreateShellItemArrayFromIDLists function


## -description


Creates a Shell item array object from a list of <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures.


## -parameters




### -param cidl [in]

Type: <b>UINT</b>

The number of elements in the array.


### -param rgpidl [in]

Type: <b>PCIDLIST_ABSOLUTE_ARRAY</b>

A list of <i>cidl</i> constant pointers to <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures.


### -param ppsiItemArray [out]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>**</b>

When this function returns, contains an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



