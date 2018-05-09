---
UID: NF:winddi.EngUnicodeToMultiByteN
title: EngUnicodeToMultiByteN function
author: windows-driver-content
description: The EngUnicodeToMultiByteN function converts the specified Unicode string into an ANSI string using the current ANSI code page.
old-location: display\engunicodetomultibyten.htm
old-project: display
ms.assetid: 5c36322f-7a88-4c24-9f98-aaf3d30f3be4
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: EngUnicodeToMultiByteN, EngUnicodeToMultiByteN function [Display Devices], display.engunicodetomultibyten, gdifncs_4c6f2a59-787b-48a8-9676-c9a88f4201f4.xml, winddi/EngUnicodeToMultiByteN
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
-	EngUnicodeToMultiByteN
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

