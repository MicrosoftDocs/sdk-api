---
UID: NF:vfw.MCIWndPutSource
title: MCIWndPutSource macro
author: windows-sdk-content
description: The MCIWndPutSource macro redefines the coordinates of the source rectangle used for cropping the images of an AVI file during playback. You can use this macro or explicitly send the MCIWNDM_PUT_SOURCE message.
old-location: multimedia\mciwndputsource.htm
tech.root: Multimedia
ms.assetid: a55e72e3-47af-4846-a20d-5f0176127459
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: MCIWndPutSource, MCIWndPutSource macro [Windows Multimedia], _win32_MCIWndPutSource, multimedia.mciwndputsource, vfw/MCIWndPutSource
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
 - MCIWndPutSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndPutSource macro


## -description



The <b>MCIWndPutSource</b> macro redefines the coordinates of the source rectangle used for cropping the images of an AVI file during playback. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/cff95139-0302-4db3-bf2e-559e75257e85">MCIWNDM_PUT_SOURCE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param prc

Pointer to a RECT structure containing the coordinates of the source rectangle. 

