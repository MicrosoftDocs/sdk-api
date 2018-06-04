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

# EngWideCharToMultiByte function


## -description


The <b>EngWideCharToMultiByte</b> function converts a wide character string into an ANSI source string using the specified code page.


## -parameters




### -param CodePage [in]

Specifies the code page to use to perform the translation.


### -param WideCharString [in, optional]

Pointer to a buffer containing the wide character string to be translated.


### -param BytesInWideCharString [in]

Specifies the size, in bytes, of <i>WideCharString</i>.


### -param MultiByteString [out, optional]

Pointer to a buffer into which the translated character string is to be copied


### -param BytesInMultiByteString [in]

Specifies the number of bytes in <i>MultiByteString</i>. If <i>MultiByteString</i> is not large enough to contain the translation, <b>EngWideCharToMultiByte</b> truncates the string, and does not report an error.


## -returns



<b>EngWideCharToMultiByte</b> returns the number of bytes converted into multibyte form, if successful. Otherwise, it returns -1.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564980">EngMultiByteToWideChar</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565038">EngUnicodeToMultiByteN</a>
 

 

