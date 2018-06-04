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

# ShellAboutA function


## -description


Displays a <b>ShellAbout</b> dialog box.


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A window handle to a parent window. This parameter can be <b>NULL</b>.


### -param szApp [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains text to be displayed in the title bar of the <b>ShellAbout</b> dialog box and on the first line of the dialog box after the text "Microsoft". If the text contains a separator (#) that divides it into two parts, the function displays the first part in the title bar and the second part on the first line after the text "Microsoft".

                    

<b>Windows 2000, Windows XP, Windows Server 2003</b>: If the string pointed to by this parameter contains a separator (#), then the string must be writeable.

<b>Windows Vista, Windows Server 2008</b>: This string cannot exceed 200 characters in length.


### -param szOtherStuff [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains text to be displayed in the dialog box after the version and copyright information. This parameter can be <b>NULL</b>.


### -param hIcon [in, optional]

Type: <b>HICON</b>

The handle of an icon that the function displays in the dialog box. This parameter can be <b>NULL</b>, in which case the function displays the Windows icon.


## -returns



Type: <b>int</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.




## -remarks



Note that the <b>ShellAbout</b> function dialog box uses text and a default icon that are specific to Windows.

To see an example of a <b>ShellAbout</b> dialog box, choose <b>About Windows</b> from the <b>Help</b> menu drop-down list in Windows Explorer.



