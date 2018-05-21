---
UID: NF:vfw.MCIWndSetVolume
title: MCIWndSetVolume macro
author: windows-driver-content
description: The MCIWndSetVolume macro sets the volume level of an MCI device. You can use this macro or explicitly send the MCIWNDM_SETVOLUME message.
old-location: multimedia\mciwndsetvolume.htm
old-project: Multimedia
ms.assetid: 4e5da2cd-b83d-4ac3-80e1-d8ac4c6e1c42
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: MCIWndSetVolume, MCIWndSetVolume macro [Windows Multimedia], _win32_MCIWndSetVolume, multimedia.mciwndsetvolume, vfw/MCIWndSetVolume
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
-	MCIWndSetVolume
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndSetVolume macro


## -description



The <b>MCIWndSetVolume</b> macro sets the volume level of an MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/04151588-b761-447a-9a57-808c034c3059">MCIWNDM_SETVOLUME</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param iVol

New volume level. Specify 1000 for normal volume level. Specify a higher value for a louder volume or a lower value for a quieter volume. 

