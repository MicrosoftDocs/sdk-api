---
UID: NF:shlobj_core.SHCreateDefaultContextMenu
title: SHCreateDefaultContextMenu function
author: windows-sdk-content
description: Creates an object that represents the Shell's default context menu implementation.
old-location: shell\SHCreateDefaultContextMenu.htm
old-project: shell
ms.assetid: 055ff0a0-9ba7-463d-9684-3fd072b190da
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SHCreateDefaultContextMenu, SHCreateDefaultContextMenu function [Windows Shell], _shell_SHCreateDefaultContextMenu, shell.SHCreateDefaultContextMenu, shlobj_core/SHCreateDefaultContextMenu
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateDefaultContextMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHCreateDefaultContextMenu function


## -description


Creates an object that represents the Shell's default context menu implementation.


## -parameters




### -param pdcm [in]

Type: <b>const <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a>*</b>

A pointer to a constant <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a> structure.


### -param riid

Type: <b>REFIID</b>

Reference to the interface ID of the interface on which to base the object. This is typically the IID of <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a>, <a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a>, or <a href="https://msdn.microsoft.com/c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c">IContextMenu3</a>.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is typically used in the implementation of <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a>. <b>GetUIObjectOf</b> creates a context menu that merges <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> handlers specified by the <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a> structure, and can optionally provide default context menu verb implementations such as open, explore, delete, and copy.


             The operation of this function is controlled by the input specified in the <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a> structure.The API<a href="https://msdn.microsoft.com/7b5e012d-1c8b-42c5-8181-9923fd389fc5">CDefFolderMenu_Create2</a> is another way to construct the default context menu implementation. It is less expressive than <b>SHCreateDefaultContextMenu</b> but it exists in platforms prior to Windows Vista.
           



