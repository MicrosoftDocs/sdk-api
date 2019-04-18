---
UID: NF:vfw.MCIWndSetActiveTimer
title: MCIWndSetActiveTimer macro (vfw.h)
author: windows-sdk-content
description: The MCIWndSetActiveTimer macro sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active. You can use this macro or explicitly send the MCIWNDM_SETACTIVETIMER message.
old-location: multimedia\mciwndsetactivetimer.htm
tech.root: Multimedia
ms.assetid: 0a0815c4-6c35-4d67-a87b-d355f9ffbf3b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MCIWndSetActiveTimer, MCIWndSetActiveTimer macro [Windows Multimedia], _win32_MCIWndSetActiveTimer, multimedia.mciwndsetactivetimer, vfw/MCIWndSetActiveTimer
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
 - MCIWndSetActiveTimer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndSetActiveTimer macro


## -description



The <b>MCIWndSetActiveTimer</b> macro sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/a30c0091-d9bb-44a3-a7b0-d1be30adcd9c">MCIWNDM_SETACTIVETIMER</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param active

Update period, in milliseconds. The default is 500 milliseconds. 

