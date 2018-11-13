---
UID: NF:vfw.MCIWndGetSource
title: MCIWndGetSource macro
author: windows-sdk-content
description: The MCIWndGetSource macro retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback. You can use this macro or explicitly send the MCIWNDM_GET_SOURCE message.
old-location: multimedia\mciwndgetsource.htm
tech.root: Multimedia
ms.assetid: 3ac01055-7d17-499f-af2e-e50fc08e5520
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: MCIWndGetSource, MCIWndGetSource macro [Windows Multimedia], _win32_MCIWndGetSource, multimedia.mciwndgetsource, vfw/MCIWndGetSource
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
 - MCIWndGetSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndGetSource macro


## -description



The <b>MCIWndGetSource</b> macro retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/d5f25926-5a3d-412e-8248-fbf307583757">MCIWNDM_GET_SOURCE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param prc

Pointer to a RECT structure to contain the coordinates of the source rectangle. 


## -see-also




<a href="https://msdn.microsoft.com/d5f25926-5a3d-412e-8248-fbf307583757">MCIWNDM_GET_SOURCE</a>
 

 

