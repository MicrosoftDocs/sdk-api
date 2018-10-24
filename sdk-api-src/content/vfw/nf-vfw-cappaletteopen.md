---
UID: NF:vfw.capPaletteOpen
title: capPaletteOpen macro
author: windows-sdk-content
description: The capPaletteOpen macro loads a new palette from a palette file and passes it to a capture driver.
old-location: multimedia\cappaletteopen.htm
tech.root: Multimedia
ms.assetid: 1d50795e-c414-4bf5-a255-76532a34d944
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "_win32_capPaletteOpen, capPaletteOpen, capPaletteOpen macro [Windows Multimedia], multimedia.cappaletteopen, vfw/capPaletteOpen"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - capPaletteOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capPaletteOpen macro


## -description



The <b>capPaletteOpen</b> macro loads a new palette from a palette file and passes it to a capture driver. Palette files typically use the filename extension .PAL. A capture driver uses a palette when required by the specified digitized image format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/e77b518e-ff03-4622-978f-d9ebaa49c6a4">WM_CAP_PAL_OPEN</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to a null-terminated string containing the palette filename. 


## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

