---
UID: NF:vfw.capPaletteSave
title: capPaletteSave macro
author: windows-driver-content
description: The capPaletteSave macro saves the current palette to a palette file. Palette files typically use the filename extension .PAL. You can use this macro or explicitly send the WM_CAP_PAL_SAVE message.
old-location: multimedia\cappalettesave.htm
old-project: Multimedia
ms.assetid: 11309b32-bc42-41fd-a0cd-e356caade849
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "_win32_capPaletteSave, capPaletteSave, capPaletteSave macro [Windows Multimedia], multimedia.cappalettesave, vfw/capPaletteSave"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	capPaletteSave
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capPaletteSave macro


## -description



The <b>capPaletteSave</b> macro saves the current palette to a palette file. Palette files typically use the filename extension .PAL. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/b1fa3978-9147-403f-aa08-db1a803aa5ac">WM_CAP_PAL_SAVE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to a null-terminated string containing the palette filename. 


## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

