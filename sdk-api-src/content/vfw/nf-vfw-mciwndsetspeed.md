---
UID: NF:vfw.MCIWndSetSpeed
title: MCIWndSetSpeed macro (vfw.h)
author: windows-sdk-content
description: The MCIWndSetSpeed macro sets the playback speed of an MCI device. You can use this macro or explicitly send the MCIWNDM_SETSPEED message.
old-location: multimedia\mciwndsetspeed.htm
tech.root: Multimedia
ms.assetid: aaf45d2f-3f6c-4b87-82fe-3fca3f36f57d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MCIWndSetSpeed, MCIWndSetSpeed macro [Windows Multimedia], _win32_MCIWndSetSpeed, multimedia.mciwndsetspeed, vfw/MCIWndSetSpeed
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
 - MCIWndSetSpeed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndSetSpeed macro


## -description



The <b>MCIWndSetSpeed</b> macro sets the playback speed of an MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/7658dd25-dc68-4bd1-b995-df06b509be16">MCIWNDM_SETSPEED</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param iSpeed

Playback speed. Specify 1000 for normal speed, larger values for faster speeds, and smaller values for slower speeds. 

