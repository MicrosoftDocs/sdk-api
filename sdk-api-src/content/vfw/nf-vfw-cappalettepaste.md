---
UID: NF:vfw.capPalettePaste
title: capPalettePaste macro
author: windows-sdk-content
description: The capPalettePaste macro copies the palette from the clipboard and passes it to a capture driver. You can use this macro or explicitly call the WM_CAP_PAL_PASTE message.
old-location: multimedia\cappalettepaste.htm
old-project: Multimedia
ms.assetid: ccdaf58d-3d06-46c5-a812-322364a7f851
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_win32_capPalettePaste, capPalettePaste, capPalettePaste macro [Windows Multimedia], multimedia.cappalettepaste, vfw/capPalettePaste"
ms.prod: windows
ms.technology: windows-sdk
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
-	capPalettePaste
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capPalettePaste macro


## -description



The <b>capPalettePaste</b> macro copies the palette from the clipboard and passes it to a capture driver. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/d49c7fd9-be40-4a07-8339-b85f7c4c331e">WM_CAP_PAL_PASTE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



A capture driver uses a palette when required by the specified digitized video format.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

