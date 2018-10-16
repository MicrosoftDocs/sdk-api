---
UID: NF:vfw.MCIWndSetPalette
title: MCIWndSetPalette macro
author: windows-sdk-content
description: The MCIWndSetPalette macro sends a palette handle to the MCI device associated with the MCIWnd window. You can use this macro or explicitly send the MCIWNDM_SETPALETTE message.
old-location: multimedia\mciwndsetpalette.htm
tech.root: Multimedia
ms.assetid: dba9370b-2412-47b2-a140-bc787a448024
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: MCIWndSetPalette, MCIWndSetPalette macro [Windows Multimedia], _win32_MCIWndSetPalette, multimedia.mciwndsetpalette, vfw/MCIWndSetPalette
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
 - MCIWndSetPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndSetPalette macro


## -description



The <b>MCIWndSetPalette</b> macro sends a palette handle to the MCI device associated with the MCIWnd window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/d2399cb7-d83c-465c-b02f-e6a016c28ae3">MCIWNDM_SETPALETTE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param hpal

Palette handle. 

