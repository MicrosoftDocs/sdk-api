---
UID: NF:vfw.MCIWndGetError
title: MCIWndGetError macro
author: windows-sdk-content
description: The MCIWndGetError macro retrieves the last MCI error encountered. You can use this macro or explicitly send the MCIWNDM_GETERROR message.
old-location: multimedia\mciwndgeterror.htm
tech.root: Multimedia
ms.assetid: 67cbd522-2409-4eeb-b62b-d78f8caea349
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: MCIWndGetError, MCIWndGetError macro [Windows Multimedia], _win32_MCIWndGetError, multimedia.mciwndgeterror, vfw/MCIWndGetError
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
 - MCIWndGetError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndGetError macro


## -description



The <b>MCIWndGetError</b> macro retrieves the last MCI error encountered. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/f110a9b3-5b05-4bf0-85d1-b49ce7396222">MCIWNDM_GETERROR</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to an application-defined buffer used to return the error string. 


### -param len

Size, in bytes, of the error buffer. 


## -remarks



If <i>lp</i> is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer. If the error string is longer than the buffer, MCIWnd truncates it.




## -see-also




<a href="https://msdn.microsoft.com/f110a9b3-5b05-4bf0-85d1-b49ce7396222">MCIWNDM_GETERROR</a>
 

 

