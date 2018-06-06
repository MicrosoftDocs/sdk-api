---
UID: NF:vfw.MCIWndPlayReverse
title: MCIWndPlayReverse macro
author: windows-sdk-content
description: The MCIWndPlayReverse macro plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback.
old-location: multimedia\mciwndplayreverse.htm
old-project: Multimedia
ms.assetid: 1f3c9c98-a8f5-4ad9-bef9-5d685076df9d
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: MCIWndPlayReverse, MCIWndPlayReverse macro [Windows Multimedia], _win32_MCIWndPlayReverse, multimedia.mciwndplayreverse, vfw/MCIWndPlayReverse
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
 - MCIWndPlayReverse
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndPlayReverse macro


## -description



The <b>MCIWndPlayReverse</b> macro plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/93a22454-eca6-453f-abbe-6cf20198dbad">MCIWNDM_PLAYREVERSE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 

