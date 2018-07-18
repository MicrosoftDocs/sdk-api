---
UID: NF:vfw.MCIWndSetRepeat
title: MCIWndSetRepeat macro
author: windows-sdk-content
description: The MCIWndSetRepeat macro sets the repeat flag associated with continuous playback. You can use this macro or explicitly send the MCIWNDM_SETREPEAT message.
old-location: multimedia\mciwndsetrepeat.htm
old-project: Multimedia
ms.assetid: e9c64f01-dd51-4f45-bf58-e930d5d23461
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: MCIWndSetRepeat, MCIWndSetRepeat macro [Windows Multimedia], _win32_MCIWndSetRepeat, multimedia.mciwndsetrepeat, vfw/MCIWndSetRepeat
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
 - MCIWndSetRepeat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndSetRepeat macro


## -description



The <b>MCIWndSetRepeat</b> macro sets the repeat flag associated with continuous playback. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/9a8da201-9ce8-4b6c-8b76-cd9e1356c75d">MCIWNDM_SETREPEAT</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param f

New state of the repeat flag. Specify <b>TRUE</b> to turn on continuous playback. 


## -remarks



The <b>MCIWndSetRepeat</b> macro only affects playback that the user initiates by hitting the play button on the toolbar. It will not affect playback started with the <b>MCIWndPlay</b> macro.

Currently, MCIAVI is the only device that supports continuous playback.



