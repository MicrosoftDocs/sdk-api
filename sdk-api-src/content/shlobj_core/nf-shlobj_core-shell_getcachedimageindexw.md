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

# Shell_GetCachedImageIndexW function


## -description


<p class="CCE_Message">[<b>Shell_GetCachedImageIndex</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <b>Shell_GetCachedImageIndexA</b> or <b>Shell_GetCachedImageIndexW</b>.]

Retrieves the cache index of a cached icon.


## -parameters




### -param pszIconPath

TBD


### -param iIconIndex

Type: <b>int</b>

The index of the image within the file named at <i>pwszIconPath</i>.


### -param uIconFlags

Type: <b>UINT</b>

Not used.


#### - pwszIconPath [in]

Type: <b>PCWSTR</b>

A pointer to a buffer that contains the path to the image file.


## -returns



Type: <b>int</b>

Returns the index of the image, or –1 on failure.




## -remarks



The <b>Shell_GetCachedImageIndexA</b> and <b>Shell_GetCachedImageIndexW</b> versions of this function were added in Windows Vista. For Unicode strings, call either <b>Shell_GetCachedImageIndexW</b> or <b>Shell_GetCachedImageIndex</b>. For ANSI strings, you must call <b>Shell_GetCachedImageIndexA</b> explicitly.

<b>Windows Server 2003 and Windows XP:  </b>Only <b>Shell_GetCachedImageIndex</b> is supported. <b>Shell_GetCachedImageIndex</b> requires a Unicode string.




## -see-also




<a href="https://msdn.microsoft.com/4e661326-157e-4c75-86df-cd213e01c3e5">FileIconInit</a>
 

 

