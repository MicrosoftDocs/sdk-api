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

# EngUnicodeToMultiByteN function


## -description


The <b>EngUnicodeToMultiByteN</b> function converts the specified Unicode string into an ANSI string using the current ANSI code page.


## -parameters




### -param MultiByteString [out]

Pointer to the buffer that receives the resultant ANSI string.


### -param MaxBytesInMultiByteString [in]

Specifies the maximum number of bytes to be written to <i>MultiByteString. </i>If this value is too small, causing <i>MultiByteString</i> to be a truncated equivalent of <i>UnicodeString</i>, then no error condition results.


### -param BytesInMultiByteString [out, optional]

Pointer to a ULONG that receives the number of bytes written to <i>MultiByteString</i>.


### -param UnicodeString [in]

Pointer to the Unicode source string that is to be converted to ANSI.


### -param BytesInUnicodeString [in]

Specifies the number of bytes in <i>UnicodeString.</i>


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564979">EngMultiByteToUnicodeN</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565466">EngWideCharToMultiByte</a>
 

 

