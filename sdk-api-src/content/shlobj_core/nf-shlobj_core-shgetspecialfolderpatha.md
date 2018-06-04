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

# SHGetSpecialFolderPathA function


## -description


<p class="CCE_Message">[<b>SHGetSpecialFolderPath</b> is not supported. Instead, use <a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">ShGetFolderPath</a>.]

Retrieves the path of a special folder, identified by its <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a>.


## -parameters




### -param hwnd

TBD


### -param pszPath

TBD


### -param csidl [in]

Type: <b>int</b>

A <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> that identifies the folder of interest. If a virtual folder is specified, this function will fail.


### -param fCreate [in]

Type: <b>BOOL</b>

Indicates whether the folder should be created if it does not already exist. If this value is nonzero, the folder is created. If this value is zero, the folder is not created.


#### - hwndOwner

Type: <b>HWND</b>

Reserved.


#### - lpszPath [out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string that receives the drive and path of the specified folder. This buffer must be at least MAX_PATH characters in size.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.




## -remarks



The Microsoft Internet Explorer 4.0 Desktop Update must be installed for this function to be available.



