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

# TextRenderingHint enumeration


## -description


The <b>TextRenderingHint</b> enumeration specifies the process used to render text. The process affects the quality of the text.


## -enum-fields




### -field TextRenderingHintSystemDefault

Specifies that a character is drawn using the currently selected system font smoothing mode (also called a rendering hint). 


### -field TextRenderingHintSingleBitPerPixelGridFit

Specifies that a character is drawn using its glyph bitmap and hinting to improve character appearance on stems and curvature. 


### -field TextRenderingHintSingleBitPerPixel

Specifies that a character is drawn using its glyph bitmap and no hinting. This results in better performance at the expense of quality. 


### -field TextRenderingHintAntiAliasGridFit

Specifies that a character is drawn using its antialiased glyph bitmap and hinting. This results in much better quality due to antialiasing at a higher performance cost. 


### -field TextRenderingHintAntiAlias

Specifies that a character is drawn using its antialiased glyph bitmap and no hinting. Stem width differences may be noticeable because hinting is turned off. 


### -field TextRenderingHintClearTypeGridFit

Specifies that a character is drawn using its glyph ClearType bitmap and hinting. This type of text rendering cannot be used along with <a href="https://msdn.microsoft.com/5bc2691d-8d7d-4322-bdae-a3b8ceb2d963">CompositingModeSourceCopy</a>. 
				

Windows XP and Windows Server 2003 and later versions of Windows only: ClearType rendering is supported only on Windows XP and Windows Server 2003 and later versions of Windows. Therefore, <a href="https://msdn.microsoft.com/7f0c88f2-106f-4045-a6eb-cd84cab150c4">TextRenderingHintClearTypeGridFit</a> is ignored on other operating systems even though GDI+ is supported on those operating systems.


## -remarks



The quality associated with each process varies according to the circumstances. <b><b>TextRenderingHintClearTypeGridFit</b></b> provides the best quality for most LCD monitors and relatively small font sizes. <b><b>TextRenderingHintAntiAlias</b></b> provides the best quality for rotated text. Generally, a process that produces higher quality text is slower than a process that produces lower quality text.




## -see-also




<a href="https://msdn.microsoft.com/780d97ec-f446-4d19-837f-517a7d6dd27d">Antialiasing with Text</a>



<a href="https://msdn.microsoft.com/5bc2691d-8d7d-4322-bdae-a3b8ceb2d963">CompositingMode</a>



<a href="https://msdn.microsoft.com/b3568ed9-e359-4916-a83d-7553c021d197">DrawString Methods</a>



<a href="https://msdn.microsoft.com/6525ac0e-bfd7-4471-bedb-df970b208222">Graphics::GetTextRenderingHint</a>



<a href="https://msdn.microsoft.com/6ea9da15-a894-4b88-8615-bdfec19f4c1c">Graphics::SetTextRenderingHint</a>
 

 

