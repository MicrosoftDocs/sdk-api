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

# EngMultiByteToWideChar function


## -description


The <b>EngMultiByteToWideChar</b> function converts an ANSI source string into a wide character string using the specified code page.


## -parameters




### -param CodePage [in]

Specifies the code page to use to perform the translation.


### -param WideCharString [out, optional]

Pointer to the buffer into which the translated character string is copied.


### -param BytesInWideCharString [in]

Specifies the size, in bytes, of <i>WideCharString</i>. If <i>WideCharString</i> is not large enough to contain the translation, <b>EngMultiByteToWideChar</b> truncates the string, and does not report an error.


### -param MultiByteString [in, optional]

Pointer to the buffer containing the multibyte string to be translated.


### -param BytesInMultiByteString [in]

Specifies the number of bytes in <i>MultiByteString.</i>


## -returns



The <b>EngMultiByteToWideChar</b> function returns the number of bytes it converted to wide character form, if successful. Otherwise, the function returns -1.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565038">EngUnicodeToMultiByteN</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565466">EngWideCharToMultiByte</a>
 

 

