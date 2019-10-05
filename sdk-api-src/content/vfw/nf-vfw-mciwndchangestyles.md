---
UID: NF:vfw.MCIWndChangeStyles
title: MCIWndChangeStyles macro (vfw.h)
author: windows-sdk-content
description: The MCIWndChangeStyles macro changes the styles used by the MCIWnd window. You can use this macro or explicitly send the MCIWNDM_CHANGESTYLES message.
old-location: multimedia\mciwndchangestyles.htm
tech.root: Multimedia
ms.assetid: d87da0b0-4217-421d-a9d5-03602fb2b477
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MCIWndChangeStyles, MCIWndChangeStyles macro [Windows Multimedia], _win32_MCIWndChangeStyles, multimedia.mciwndchangestyles, vfw/MCIWndChangeStyles
ms.topic: macro
f1_keywords: 
 - "vfw/MCIWndChangeStyles"
dev_langs:
 - c++
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
 - MCIWndChangeStyles
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndChangeStyles macro


## -description



The <b>MCIWndChangeStyles</b> macro changes the styles used by the MCIWnd window. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-changestyles">MCIWNDM_CHANGESTYLES</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param mask

Mask that identifies the styles that can change. This mask is the bitwise OR operator of all styles that will be permitted to change. 


### -param value

New style settings for the window. Specify zero for this parameter to turn off all styles identified in the mask. For a list of the available styles, see the MCIWndCreate function. 


## -remarks



For an example of using <b>MCIWndChangeStyles</b>, see <a href="https://docs.microsoft.com/windows/desktop/Multimedia/pausing-and-resuming-playback">Pausing and Resuming Playback</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-changestyles">MCIWNDM_CHANGESTYLES</a>
 

 

