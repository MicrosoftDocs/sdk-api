---
UID: NF:vfw.MCIWndGetDevice
title: MCIWndGetDevice macro (vfw.h)
author: windows-sdk-content
description: The MCIWndGetDevice macro retrieves the name of the current MCI device. You can use this macro or explicitly send the MCIWNDM_GETDEVICE message.
old-location: multimedia\mciwndgetdevice.htm
tech.root: Multimedia
ms.assetid: 0e918cf0-e9aa-402a-9db6-f9a39c718962
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MCIWndGetDevice, MCIWndGetDevice macro [Windows Multimedia], _win32_MCIWndGetDevice, multimedia.mciwndgetdevice, vfw/MCIWndGetDevice
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
 - MCIWndGetDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndGetDevice macro


## -description



The <b>MCIWndGetDevice</b> macro retrieves the name of the current MCI device. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-getdevice">MCIWNDM_GETDEVICE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to an application-defined buffer to return the device name. 


### -param len

Size, in bytes, of the buffer. 


## -remarks



If the null-terminated string containing the device name is longer than the buffer, MCIWnd truncates it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-getdevice">MCIWNDM_GETDEVICE</a>
 

 

