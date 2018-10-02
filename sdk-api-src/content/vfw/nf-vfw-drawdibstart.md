---
UID: NF:vfw.DrawDibStart
title: DrawDibStart function
author: windows-sdk-content
description: The DrawDibStart function prepares a DrawDib DC for streaming playback.
old-location: multimedia\drawdibstart.htm
tech.root: Multimedia
ms.assetid: 2c992a4f-3308-4f0a-a1cf-40515e28ae33
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DrawDibStart, DrawDibStart function [Windows Multimedia], _win32_DrawDibStart, multimedia.drawdibstart, vfw/DrawDibStart
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrawDibStart function


## -description



The <b>DrawDibStart</b> function prepares a DrawDib DC for streaming playback.




## -parameters




### -param hdd

Handle to a DrawDib DC.


### -param rate

Playback rate, in microseconds per frame.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

