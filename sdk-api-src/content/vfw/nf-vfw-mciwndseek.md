---
UID: NF:vfw.MCIWndSeek
title: MCIWndSeek macro
author: windows-sdk-content
description: The MCIWndSeek macro moves the playback position to the specified location in the content. You can use this macro or explicitly use the MCI_SEEK command.
old-location: multimedia\mciwndseek.htm
old-project: Multimedia
ms.assetid: 96d42e1a-03d5-4007-95d8-0e4b8d2018d5
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: MCIWndSeek, MCIWndSeek macro [Windows Multimedia], _win32_MCIWndSeek, multimedia.mciwndseek, vfw/MCIWndSeek
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	MCIWndSeek
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndSeek macro


## -description



The <b>MCIWndSeek</b> macro moves the playback position to the specified location in the content. You can use this macro or explicitly use the <a href="https://msdn.microsoft.com/5ffab964-a28d-4dc2-ac04-da501cd34d24">MCI_SEEK</a> command.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lPos

Position to seek. You can specify a position using the current time format, the MCIWND_START constant to designate the beginning of the content, or the MCIWND_END constant to designate the end of the content. 

