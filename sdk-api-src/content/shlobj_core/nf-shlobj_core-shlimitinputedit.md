---
UID: NF:shlobj_core.SHLimitInputEdit
title: SHLimitInputEdit function
author: windows-sdk-content
description: Sets limits on valid characters for an edit control.
old-location: shell\SHLimitInputEdit.htm
old-project: shell
ms.assetid: 3f03374f-8dfe-4b80-9ecc-12c6548f2865
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: SHLimitInputEdit, SHLimitInputEdit function [Windows Shell], _shell_SHLimitInputEdit, shell.SHLimitInputEdit, shlobj_core/SHLimitInputEdit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
api_name:
 - SHLimitInputEdit
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHLimitInputEdit function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Sets limits on valid characters for an edit control.


## -parameters




### -param hwndEdit [in, optional]

Type: <b>HWND</b>

The handle of the edit control.


### -param psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

An <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface pointer. This object must also implement <a href="https://msdn.microsoft.com/2850bdf1-12ea-42cd-a0fb-68491337ae69">IItemNameLimits</a>, which supplies a list of invalid characters and a maximum name length.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



