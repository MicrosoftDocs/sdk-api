---
UID: NF:wingdi.GetTextCharset
title: GetTextCharset function
author: windows-driver-content
description: Retrieves a character set identifier for the font that is currently selected into a specified device context.
old-location: intl\gettextcharset.htm
old-project: Intl
ms.assetid: 11040353-a2ea-42fe-aa89-3438ffc1fea6
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetTextCharset, GetTextCharset function [Internationalization for Windows Applications], _win32_GetTextCharset, intl.gettextcharset, wingdi/GetTextCharset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FAX_TIME, *PFAX_TIME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Gdi32.dll
-	Ext-MS-Win-GDI-Font-l1-1-2.dll
-	Ext-MS-Win-GDI-Font-L1-1-3.dll
-	GDI32Full.dll
api_name:
-	GetTextCharset
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetTextCharset function


## -description


Retrieves a character set identifier for the font that is currently selected into a specified device context.
<div class="alert"><b>Note</b>  A call to this function is equivalent to a call to <a href="https://msdn.microsoft.com/1c8c114a-b261-457c-b541-4648a8f38ee8">GetTextCharsetInfo</a> passing <b>NULL</b> for the data buffer.</div><div> </div>

## -parameters




### -param hdc [in]

Handle to a device context. The function obtains a character set identifier for the font that is selected into this device context.


## -returns



If successful, returns a value identifying the character set of the font that is currently selected into the specified device context. The following character set identifiers are defined:

If the function fails, it returns DEFAULT_CHARSET.




## -see-also




<a href="https://msdn.microsoft.com/1c8c114a-b261-457c-b541-4648a8f38ee8">GetTextCharsetInfo</a>



<a href="https://msdn.microsoft.com/1799f5da-1391-4b6e-ac13-718017a77557">Unicode and Character Set Functions</a>



<a href="https://msdn.microsoft.com/8c1c6582-b58c-4008-9ce5-208acc191d9f">Unicode and Character Sets</a>
 

 

