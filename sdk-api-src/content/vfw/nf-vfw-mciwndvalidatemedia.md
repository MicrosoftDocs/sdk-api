---
UID: NF:vfw.MCIWndValidateMedia
title: MCIWndValidateMedia macro
author: windows-driver-content
description: The MCIWndValidateMedia macro updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format.
old-location: multimedia\mciwndvalidatemedia.htm
old-project: Multimedia
ms.assetid: 25dc3d0c-6718-4155-9a60-e140da0473e8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MCIWndValidateMedia, MCIWndValidateMedia macro [Windows Multimedia], _win32_MCIWndValidateMedia, multimedia.mciwndvalidatemedia, vfw/MCIWndValidateMedia
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
-	MCIWndValidateMedia
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndValidateMedia macro


## -description



The <b>MCIWndValidateMedia</b> macro updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/98ac6227-fc90-4276-8e26-2bd005e35dc6">MCIWNDM_VALIDATEMEDIA</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -remarks



Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format. You can use this macro to update these values.



