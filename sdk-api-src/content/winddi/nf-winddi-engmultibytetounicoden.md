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

# EngMultiByteToUnicodeN function


## -description


The <b>EngMultiByteToUnicodeN</b> function converts the specified ANSI source string into a Unicode string using the current ANSI code page.


## -parameters




### -param UnicodeString [out]

Pointer to the buffer that receives the resultant Unicode string.


### -param MaxBytesInUnicodeString [in]

Supplies the maximum number of bytes to be written to <i>UnicodeString. </i>If this value is too small, causing <i>UnicodeString</i> to be a truncated equivalent of <i>MultiByteString</i>, no error condition results.


### -param BytesInUnicodeString [out, optional]

Pointer to a ULONG that receives the number of bytes written to <i>UnicodeString</i>.


### -param MultiByteString [in]

Pointer to the ANSI source string that is to be converted to Unicode.


### -param BytesInMultiByteString [in]

Specifies the number of bytes in <i>MultiByteString.</i>


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564980">EngMultiByteToWideChar</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565038">EngUnicodeToMultiByteN</a>
 

 

