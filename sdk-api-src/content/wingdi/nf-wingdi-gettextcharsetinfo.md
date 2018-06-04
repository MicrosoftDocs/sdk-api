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
 

 

