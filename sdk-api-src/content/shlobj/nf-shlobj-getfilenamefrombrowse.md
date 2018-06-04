---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetFileNameFromBrowse function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Creates an <b>Open</b> dialog box so that the user can specify the drive, directory, and name of a file to open.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box. This member can be any valid window handle, or it can be <b>NULL</b> if the dialog box has no owner.


### -param pszFilePath [in, out]

Type: <b>PWSTR</b>

A null-terminated Unicode string that contains a file name used to initialize the File Name edit control. This string corresponds to the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure's <b>lpstrFile</b> member and is used in exactly the same way.


### -param cchFilePath

Type: <b>UINT</b>

The number of characters in <i>pszFilePath</i>, including the terminating null character.


### -param pszWorkingDir [in, optional]

Type: <b>PCWSTR</b>

The fully qualified file path of the initial directory. This string corresponds to the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure's <b>lpstrInitialDir</b> member and is used in exactly the same way.


### -param pszDefExt [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the default file name extension. This extension is added to <i>pszFilePath</i> if the user does not specify an extension. The string should not contain any '.' characters. If this string is <b>NULL</b> and the user fails to type an extension, no extension is appended.


### -param pszFilters [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that defines the filter. This string corresponds to the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure's <b>lpstrFilter</b> member and is used in exactly the same way.


### -param pszTitle

TBD




#### - szTitle [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that is placed in the title bar of the dialog box. If this value is <b>NULL</b>, the system uses the default title.


## -returns



Type: <b>BOOL</b>

If the user specifies a file name and clicks <b>OK</b>, the return value is <b>TRUE</b>. The buffer that <i>pszFilePath</i> points to contains the full path and file name that the user specifies. If the user cancels or closes the <b>Open</b> dialog box or an error occurs, the return value is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/22b8f3d0-455a-4eb8-9835-e90d41924ec7">GetOpenFileName</a>
 

 

