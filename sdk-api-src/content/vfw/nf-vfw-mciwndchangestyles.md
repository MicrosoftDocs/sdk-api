---
UID: NF:vfw.MCIWndChangeStyles
title: MCIWndChangeStyles macro
author: windows-sdk-content
description: The MCIWndChangeStyles macro changes the styles used by the MCIWnd window. You can use this macro or explicitly send the MCIWNDM_CHANGESTYLES message.
old-location: multimedia\mciwndchangestyles.htm
tech.root: Multimedia
ms.assetid: d87da0b0-4217-421d-a9d5-03602fb2b477
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: MCIWndChangeStyles, MCIWndChangeStyles macro [Windows Multimedia], _win32_MCIWndChangeStyles, multimedia.mciwndchangestyles, vfw/MCIWndChangeStyles
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
 - MCIWndChangeStyles
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
- MCIWndChangeStyles
: 
---

# MCIWndChangeStyles macro


## -description



The <b>MCIWndChangeStyles</b> macro changes the styles used by the MCIWnd window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/9074c21a-e49f-4089-a6d2-af8d513cb632">MCIWNDM_CHANGESTYLES</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param mask

Mask that identifies the styles that can change. This mask is the bitwise OR operator of all styles that will be permitted to change. 


### -param value

New style settings for the window. Specify zero for this parameter to turn off all styles identified in the mask. For a list of the available styles, see the MCIWndCreate function. 


## -remarks



For an example of using <b>MCIWndChangeStyles</b>, see <a href="https://msdn.microsoft.com/f5a7ef22-993c-4aab-bab0-2700289da7a7">Pausing and Resuming Playback</a>.




## -see-also




<a href="https://msdn.microsoft.com/9074c21a-e49f-4089-a6d2-af8d513cb632">MCIWNDM_CHANGESTYLES</a>
 

 

