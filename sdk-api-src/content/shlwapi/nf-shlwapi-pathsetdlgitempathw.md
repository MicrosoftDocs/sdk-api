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

# PathSetDlgItemPathW function


## -description


Sets the text of a child control in a window or dialog box, using <a href="https://msdn.microsoft.com/b8184c98-1f86-4714-baf8-af4ef3e71cf2">PathCompactPath</a> to ensure the path fits in the control.


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box or window.


### -param id [in]

Type: <b>int</b>

The identifier of the control.


### -param pszPath [in]

Type: <b>LPCSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to set in the control.


## -returns



This function does not return a value.



