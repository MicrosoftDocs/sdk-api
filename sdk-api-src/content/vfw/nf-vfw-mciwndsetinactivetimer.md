---
UID: NF:vfw.MCIWndSetInactiveTimer
title: MCIWndSetInactiveTimer macro
author: windows-sdk-content
description: The MCIWndSetInactiveTimer macro sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive. You can use this macro or explicitly send the MCIWNDM_SETINACTIVETIMER message.
old-location: multimedia\mciwndsetinactivetimer.htm
tech.root: Multimedia
ms.assetid: 2a0d45dc-1df6-4b1a-b4bc-3704257c5b38
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MCIWndSetInactiveTimer, MCIWndSetInactiveTimer macro [Windows Multimedia], _win32_MCIWndSetInactiveTimer, multimedia.mciwndsetinactivetimer, vfw/MCIWndSetInactiveTimer
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
 - MCIWndSetInactiveTimer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- vfw.h
: 
- MCIWndSetInactiveTimer
: 
---

# MCIWndSetInactiveTimer macro


## -description



The <b>MCIWndSetInactiveTimer</b> macro sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/8900c372-0493-4a63-a027-ef6ecf8f8254">MCIWNDM_SETINACTIVETIMER</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param inactive

Update period, in milliseconds. The default is 2000 milliseconds. 

