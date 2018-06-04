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

# StrFormatKBSizeA function


## -description


Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.


## -parameters




### -param qdw

Type: <b>LONGLONG</b>

The numeric value to be converted.


### -param pszBuf [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the converted number.


### -param cchBuf

Type: <b>UINT</b>

The size of <i>pszBuf</i>, in characters.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to the converted string, or <b>NULL</b> if the conversion fails.




## -remarks



In Windows 10, size is reported in base 10 rather than  base 2. For example, 1 KB is 1000 bytes rather than 1024.




## -see-also




<a href="https://msdn.microsoft.com/244f93cb-0976-4a31-958c-ae0ed81c1dcf">StrFormatByteSizeA</a>



<a href="https://msdn.microsoft.com/00192755-9135-4193-90bc-6e312b294007">StrFormatByteSizeW</a>
 

 

