---
UID: NF:vfw.MCIWndGetDest
title: MCIWndGetDest macro
author: windows-sdk-content
description: The MCIWndGetDest macro retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback. You can use this macro or explicitly send the MCIWNDM_GET_DEST message.
old-location: multimedia\mciwndgetdest.htm
tech.root: Multimedia
ms.assetid: eca70819-fb7c-48b9-a479-d20aa0f05649
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MCIWndGetDest, MCIWndGetDest macro [Windows Multimedia], _win32_MCIWndGetDest, multimedia.mciwndgetdest, vfw/MCIWndGetDest
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
 - MCIWndGetDest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndGetDest macro


## -description



The <b>MCIWndGetDest</b> macro retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/d4d8a3eb-aad4-4435-a23b-7a9c55fc194d">MCIWNDM_GET_DEST</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param prc

Pointer to a RECT structure to return the coordinates of the destination rectangle. 


## -see-also




<a href="https://msdn.microsoft.com/d4d8a3eb-aad4-4435-a23b-7a9c55fc194d">MCIWNDM_GET_DEST</a>
 

 

