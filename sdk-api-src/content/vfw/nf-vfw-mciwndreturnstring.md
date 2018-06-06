---
UID: NF:vfw.MCIWndReturnString
title: MCIWndReturnString macro
author: windows-sdk-content
description: The MCIWndReturnString macro retrieves the reply to the most recent MCI string command sent to an MCI device. Information in the reply is supplied as a null-terminated string. You can use this macro or explicitly send the MCIWNDM_RETURNSTRING message.
old-location: multimedia\mciwndreturnstring.htm
old-project: Multimedia
ms.assetid: 8e7d54ec-882b-4896-a493-3ed61aec6184
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: MCIWndReturnString, MCIWndReturnString macro [Windows Multimedia], _win32_MCIWndReturnString, multimedia.mciwndreturnstring, vfw/MCIWndReturnString
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndReturnString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndReturnString macro


## -description



The <b>MCIWndReturnString</b> macro retrieves the reply to the most recent MCI string command sent to an MCI device. Information in the reply is supplied as a null-terminated string. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/36a5222c-a63c-4b8c-ad0c-a00477e95b96">MCIWNDM_RETURNSTRING</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to an application-defined buffer to contain the null-terminated string. 


### -param len

Size, in bytes, of the buffer. 


## -remarks



If the null-terminated string is longer than the buffer, the string is truncated.



