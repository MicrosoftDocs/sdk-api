---
UID: NF:vfw.MCIWndPutDest
title: MCIWndPutDest macro
author: windows-sdk-content
description: The MCIWndPutDest macro redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback. You can use this macro or explicitly send the MCIWNDM_PUT_DEST message.
old-location: multimedia\mciwndputdest.htm
tech.root: Multimedia
ms.assetid: d058c1b7-f7f8-49a0-84cc-ece298a25289
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: MCIWndPutDest, MCIWndPutDest macro [Windows Multimedia], _win32_MCIWndPutDest, multimedia.mciwndputdest, vfw/MCIWndPutDest
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
 - MCIWndPutDest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndPutDest macro


## -description



The <b>MCIWndPutDest</b> macro redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/0b13d473-ef93-41a2-bbb2-09fbf264493e">MCIWNDM_PUT_DEST</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param prc

Pointer to a RECT structure containing the coordinates of the destination rectangle. 

