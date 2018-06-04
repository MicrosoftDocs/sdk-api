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

# Win32DeleteFile function


## -description


<p class="CCE_Message">[<b>Win32DeleteFile</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Deletes a file.


## -parameters




### -param pszPath

TBD




#### - pszFileName [in]

Type: <b>PCWSTR</b>

A pointer to a buffer that contains the full name of the file to delete.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the file was successfully deleted; otherwise <b>FALSE</b>.



