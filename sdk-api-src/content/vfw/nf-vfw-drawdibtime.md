---
UID: NF:vfw.DrawDibTime
title: DrawDibTime function (vfw.h)
author: windows-sdk-content
description: The DrawDibTime function retrieves timing information about the drawing operation and is used during debug operations.
old-location: multimedia\drawdibtime.htm
tech.root: Multimedia
ms.assetid: 86dd2c5c-f853-4954-b245-6aa51d157600
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawDibTime, DrawDibTime function [Windows Multimedia], _win32_DrawDibTime, multimedia.drawdibtime, vfw/DrawDibTime
ms.topic: function
f1_keywords: ["vfw/DrawDibTime"]
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
 - DrawDibTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrawDibTime function


## -description



The <b>DrawDibTime</b> function retrieves timing information about the drawing operation and is used during debug operations.




## -parameters




### -param hdd

Handle to a DrawDib DC.
          


### -param lpddtime

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-drawdibtime">DRAWDIBTIME</a> structure.
          


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.
          




## -remarks



This function is present only in the debug version of the Microsoft Windows Software Development Kit (SDK) libraries.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>
 

 

