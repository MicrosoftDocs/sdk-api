---
UID: NF:wingdi.GetTextCharsetInfo
title: GetTextCharsetInfo function
author: windows-driver-content
description: Retrieves information about the character set of the font that is currently selected into a specified device context.
old-location: intl\gettextcharsetinfo.htm
old-project: Intl
ms.assetid: 1c8c114a-b261-457c-b541-4648a8f38ee8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetTextCharsetInfo, GetTextCharsetInfo function [Internationalization for Windows Applications], _win32_GetTextCharsetInfo, intl.gettextcharsetinfo, wingdi/GetTextCharsetInfo
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Gdi32.dll
-	Ext-MS-Win-GDI-Font-l1-1-1.dll
-	ext-ms-win-gdi-font-l1-1-2.dll
-	Ext-MS-Win-GDI-Font-L1-1-3.dll
-	GDI32Full.dll
api_name:
-	GetTextCharsetInfo
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetTextCharsetInfo function


## -description


Retrieves information about the character set of the font that is currently selected into a specified device context.


## -parameters




### -param hdc [in]

Handle to a device context. The function obtains information about the font that is selected into this device context.


### -param lpSig [out, optional]

Pointer to a <a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a> data structure that receives font-signature information.

If a TrueType font is currently selected into the device context, the <a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a> structure receives information that identifies the code page and Unicode subranges for which the font provides glyphs.

If a font other than TrueType is currently selected into the device context, the <a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a> structure receives zeros. In this case, the application should use the <a href="https://msdn.microsoft.com/0e6e81f1-ec7b-42ba-8706-a352349fa6ab">TranslateCharsetInfo</a> function to obtain generic font-signature information for the character set.

The <i>lpSig</i> parameter specifies <b>NULL</b> if the application does not require the <a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a> information. In this case, the application can also call the       <a href="https://msdn.microsoft.com/11040353-a2ea-42fe-aa89-3438ffc1fea6">GetTextCharset</a> function, which is equivalent to calling       <b>GetTextCharsetInfo</b> with <i>lpSig</i> set to <b>NULL</b>.


### -param dwFlags [in]

Reserved; must be set to 0.


## -returns



If successful, returns a value identifying the character set of the font currently selected into the specified device context. The following character set identifiers are defined:

If the function fails, the return value is DEFAULT_CHARSET.




## -see-also




<a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a>



<a href="https://msdn.microsoft.com/11040353-a2ea-42fe-aa89-3438ffc1fea6">GetTextCharset</a>



<a href="https://msdn.microsoft.com/0e6e81f1-ec7b-42ba-8706-a352349fa6ab">TranslateCharsetInfo</a>



<a href="https://msdn.microsoft.com/1799f5da-1391-4b6e-ac13-718017a77557">Unicode and Character Set Functions</a>



<a href="https://msdn.microsoft.com/8c1c6582-b58c-4008-9ce5-208acc191d9f">Unicode and Character Sets</a>
 

 

