---
UID: NF:vfw.MCIWndSetTimeFormat
title: MCIWndSetTimeFormat macro
author: windows-sdk-content
description: The MCIWndSetTimeFormat macro sets the time format of an MCI device. You can use this macro or explicitly send the MCIWNDM_SETTIMEFORMAT message.
old-location: multimedia\mciwndsettimeformat.htm
tech.root: Multimedia
ms.assetid: dcf70d76-6f53-4e05-ab05-3f9136294d7a
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: MCIWndSetTimeFormat, MCIWndSetTimeFormat macro [Windows Multimedia], _win32_MCIWndSetTimeFormat, multimedia.mciwndsettimeformat, vfw/MCIWndSetTimeFormat
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
 - MCIWndSetTimeFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndSetTimeFormat macro


## -description



The <b>MCIWndSetTimeFormat</b> macro sets the time format of an MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/7de82094-6d35-44fd-88e7-ebd18a558cfd">MCIWNDM_SETTIMEFORMAT</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to a buffer containing the null-terminated string indicating the time format. Specify "frames" to set the time format to frames, or "ms" to set the time format to milliseconds. 


## -remarks



An application can specify time formats other than frames or milliseconds as long as the formats are supported by the MCI device. Noncontinuous formats, such as tracks and SMPTE, can cause the trackbar to behave erratically. For these time formats, you might want to turn off the toolbar by using the <a href="https://msdn.microsoft.com/d87da0b0-4217-421d-a9d5-03602fb2b477">MCIWndChangeStyles</a> macro and specifying the MCIWNDF_NOPLAYBAR window style.

If you want to set the time format to frames or milliseconds, you can also use the <b>MCIWndUseFrames</b> or <b>MCIWndUseTime</b> macro. For a list of time formats, see the <b>MCIWndGetTimeFormat</b> macro.



