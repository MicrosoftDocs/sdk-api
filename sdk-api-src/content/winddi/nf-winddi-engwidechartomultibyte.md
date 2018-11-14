---
UID: NF:winddi.EngWideCharToMultiByte
title: EngWideCharToMultiByte function
author: windows-sdk-content
description: The EngWideCharToMultiByte function converts a wide character string into an ANSI source string using the specified code page.
old-location: display\engwidechartomultibyte.htm
tech.root: display
ms.assetid: db0ae856-f414-4ae9-9bc9-c719581873fd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EngWideCharToMultiByte, EngWideCharToMultiByte function [Display Devices], display.engwidechartomultibyte, gdifncs_04d04a1a-7a81-47f7-958b-47ea8f52f421.xml, winddi/EngWideCharToMultiByte
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngWideCharToMultiByte
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EngWideCharToMultiByte
: 
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




<a href="https://msdn.microsoft.com/7ed4f718-e28d-40d9-a3e0-c6961281a319">EngMultiByteToWideChar</a>



<a href="https://msdn.microsoft.com/5c36322f-7a88-4c24-9f98-aaf3d30f3be4">EngUnicodeToMultiByteN</a>
 

 

