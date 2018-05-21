---
UID: NF:winddi.EngWideCharToMultiByte
title: EngWideCharToMultiByte function
author: windows-driver-content
description: The EngWideCharToMultiByte function converts a wide character string into an ANSI source string using the specified code page.
old-location: display\engwidechartomultibyte.htm
old-project: display
ms.assetid: db0ae856-f414-4ae9-9bc9-c719581873fd
ms.author: windowsdriverdev
ms.date: 5/10/2018
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32.dll
-	GDI32Full.dll
api_name:
-	EngWideCharToMultiByte
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

