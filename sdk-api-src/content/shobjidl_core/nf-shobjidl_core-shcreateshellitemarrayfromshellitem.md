---
UID: NF:shobjidl_core.SHCreateShellItemArrayFromShellItem
title: SHCreateShellItemArrayFromShellItem function
author: windows-sdk-content
description: Creates an array of one element from a single Shell item.
old-location: shell\SHCreateShellItemArrayFromShellItem.htm
old-project: shell
ms.assetid: 93401708-6f11-474d-8009-24554f316e79
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SHCreateShellItemArrayFromShellItem, SHCreateShellItemArrayFromShellItem function [Windows Shell], _shell_SHCreateShellItemArrayFromShellItem, shell.SHCreateShellItemArrayFromShellItem, shobjidl_core/SHCreateShellItemArrayFromShellItem
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
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHCreateShellItemArrayFromShellItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHCreateShellItemArrayFromShellItem function


## -description


Creates an array of one element from a single Shell item.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object that represents the item.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IShellItemArray.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically a pointer to an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates a one-element array from a single item. To create an array from the contents of a folder, use <a href="https://msdn.microsoft.com/024ccbc7-97f1-4cb5-8588-9c9b1f747336">SHCreateShellItemArray</a>.



