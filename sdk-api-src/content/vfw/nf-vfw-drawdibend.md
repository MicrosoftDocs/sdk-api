---
UID: NF:vfw.DrawDibEnd
title: DrawDibEnd function
author: windows-sdk-content
description: The DrawDibEnd function clears the flags and other settings of a DrawDib DC that are set by the DrawDibBegin or DrawDibDraw functions.
old-location: multimedia\drawdibend.htm
tech.root: Multimedia
ms.assetid: 717f5404-b089-4556-8435-73ba5c52723a
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: DrawDibEnd, DrawDibEnd function [Windows Multimedia], _win32_DrawDibEnd, multimedia.drawdibend, vfw/DrawDibEnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vfw.h
req.include-header: 
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrawDibEnd function


## -description



The <b>DrawDibEnd</b> function clears the flags and other settings of a DrawDib DC that are set by the <a href="https://msdn.microsoft.com/89178e33-e440-49fe-9900-0baea229d289">DrawDibBegin</a> or <a href="https://msdn.microsoft.com/b503fcd8-e928-4b3c-9ff5-96b88c5fb2f4">DrawDibDraw</a> functions.




## -parameters




### -param hdd

Handle to the DrawDib DC to free.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

