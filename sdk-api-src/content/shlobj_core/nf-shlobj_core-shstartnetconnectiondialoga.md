---
UID: NF:shlobj_core.SHStartNetConnectionDialogA
title: SHStartNetConnectionDialogA function
author: windows-sdk-content
description: SHStartNetConnectionDialog may be altered or unavailable.
old-location: shell\SHStartNetConnectionDialog.htm
old-project: shell
ms.assetid: 9de9d5f4-a89f-42d2-b24e-b037694f6e92
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RESOURCETYPE_ANY, RESOURCETYPE_DISK, RESOURCETYPE_PRINT, SHStartNetConnectionDialog, SHStartNetConnectionDialog function [Windows Shell], SHStartNetConnectionDialogA, SHStartNetConnectionDialogW, _win32_SHStartNetConnectionDialog, shell.SHStartNetConnectionDialog, shlobj_core/SHStartNetConnectionDialog, shlobj_core/SHStartNetConnectionDialogA, shlobj_core/SHStartNetConnectionDialogW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHStartNetConnectionDialogW (Unicode) and SHStartNetConnectionDialogA (ANSI)
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
 - SHStartNetConnectionDialog
 - SHStartNetConnectionDialogA
 - SHStartNetConnectionDialogW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHStartNetConnectionDialogA function


## -description


<p class="CCE_Message">[<b>SHStartNetConnectionDialog</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Displays a general browsing dialog box for a network resource connection.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window.


### -param pszRemoteName [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated character string that specifies the remote network name. This value can be set to <b>NULL</b>.


### -param dwType

Type: <b>DWORD</b>

A bitfield that contains a set of flags that identify the type of resource that the dialog box is set to find. This value can contain one of the following values, defined in Winnetwk.h:



#### RESOURCETYPE_ANY (0x00000000)

All resources



#### RESOURCETYPE_DISK (0x00000001)

Disk resources



#### RESOURCETYPE_PRINT (0x00000002)

Print resources


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.



