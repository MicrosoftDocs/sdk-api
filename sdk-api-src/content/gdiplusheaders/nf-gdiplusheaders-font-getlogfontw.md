---
UID: NF:gdiplusheaders.Font.GetLogFontW
title: Font::GetLogFontW
author: windows-sdk-content
description: The Font::GetLogFontW method uses a LOGFONTW structure to get the attributes of this Font object.
old-location: gdiplus\_gdiplus_CLASS_Font_GetLogFontW_g_logfontW_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontmethods\getlogfontw.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Font class [GDI+],GetLogFontW method, Font.GetLogFontW, Font::GetLogFontW, GetLogFontW, GetLogFontW method [GDI+], GetLogFontW method [GDI+],Font class, _gdiplus_CLASS_Font_GetLogFontW_g_logfontW_, gdiplus._gdiplus_CLASS_Font_GetLogFontW_g_logfontW_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Font.GetLogFontW
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Font::GetLogFontW


## -description


The <b>Font::GetLogFontW</b> method uses a 
			<b>LOGFONTW</b> structure to get the attributes of this 
			<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a> object.


## -parameters




### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object that contains attributes of the video display. 


### -param logfontW [out]

Type: <b>LOGFONTW*</b>

Pointer to a 
					<b>LOGFONTW</b> structure variable that receives the font attributes. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 

