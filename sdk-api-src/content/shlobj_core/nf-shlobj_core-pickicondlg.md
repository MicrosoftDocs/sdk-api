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

# PickIconDlg function


## -description


<p class="CCE_Message">[<b>PickIconDlg</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Displays a dialog box that allows the user to choose an icon from the selection available embedded in a resource such as an executable or DLL file.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

The handle of the parent window. This value can be <b>NULL</b>.


### -param pszIconPath [in, out]

Type: <b>PWSTR</b>

A pointer to a string that contains the null-terminated, fully qualified path of the default resource that contains the icons. If the user chooses a different resource in the dialog, this buffer contains the path of that file when the function returns. This buffer should be at least MAX_PATH characters in length, or the returned path may be truncated. You should verify that the path is valid before using it.


### -param cchIconPath

Type: <b>UINT</b>

The number of characters in <i>pszIconPath</i>, including the terminating <b>NULL</b> character.


### -param piIconIndex [in, out, optional]

Type: <b>int*</b>

A pointer to an integer that on entry specifies the index of the initial selection and, when this function returns successfully, receives the index of the icon that was selected.


## -returns



Type: <b>int</b>

Returns 1 if successful; otherwise, 0.



