---
UID: NF:shlobj_core.SHFind_InitMenuPopup
title: SHFind_InitMenuPopup function (shlobj_core.h)
author: windows-sdk-content
description: SHFind_InitMenuPopup may be altered or unavailable.
old-location: shell\SHFind_InitMenuPopup.htm
tech.root: shell
ms.assetid: ca44bd57-6af0-45b3-9331-914e93360743
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SHFind_InitMenuPopup, SHFind_InitMenuPopup function [Windows Shell], _win32_SHFind_InitMenuPopup, shell.SHFind_InitMenuPopup, shlobj_core/SHFind_InitMenuPopup
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHFind_InitMenuPopup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHFind_InitMenuPopup function


## -description


<p class="CCE_Message">[<b>SHFind_InitMenuPopup</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves the <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> instance for the submenu of options displayed for the <b>Search</b> entry in the Classic style Start menu.


## -parameters




### -param hmenu [in]

Type: <b>HMENU</b>

The handle of the popup menu.


### -param hwndOwner [in, optional]

Type: <b>HWND</b>

The handle of the popup menu's owner window. This value can be <b>NULL</b>.


### -param idCmdFirst

Type: <b>UINT</b>

The ID of the first menu item.


### -param idCmdLast

Type: <b>UINT</b>

The ID of the last menu item.


## -returns



Type: <b><a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a>*</b>

If successful, returns an <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> pointer. On failure, returns <b>NULL</b>.



