---
UID: NF:vfw.MCIWndGetPositionString
title: MCIWndGetPositionString macro
author: windows-driver-content
description: The MCIWndGetPositionString macro retrieves the numerical value of the current position within the content of the MCI device.
old-location: multimedia\mciwndgetpositionstring.htm
old-project: Multimedia
ms.assetid: ccca1ec7-a523-4a36-bc81-9cb25cfa3aa1
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: MCIWndGetPositionString, MCIWndGetPositionString macro [Windows Multimedia], _win32_MCIWndGetPositionString, multimedia.mciwndgetpositionstring, vfw/MCIWndGetPositionString
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
-	MCIWndGetPositionString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndGetPositionString macro


## -description



The <b>MCIWndGetPositionString</b> macro retrieves the numerical value of the current position within the content of the MCI device. This macro also provides the current position in string form in an application-defined buffer. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/6dc5d3bd-8515-4514-a2a5-c1bee07f7acf">MCIWNDM_GETPOSITION</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to an application-defined buffer used to return the position. Use zero to inhibit retrieval of the position as a string. If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.



### -param len

Size, in bytes, of the buffer. If the null-terminated string is longer than the buffer, it is truncated. Use zero to inhibit retrieval of the position as a string. 


## -see-also




<a href="https://msdn.microsoft.com/6dc5d3bd-8515-4514-a2a5-c1bee07f7acf">MCIWNDM_GETPOSITION</a>
 

 

