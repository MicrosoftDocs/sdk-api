---
UID: NF:vfw.DrawDibTime
title: DrawDibTime function
author: windows-sdk-content
description: The DrawDibTime function retrieves timing information about the drawing operation and is used during debug operations.
old-location: multimedia\drawdibtime.htm
old-project: Multimedia
ms.assetid: 86dd2c5c-f853-4954-b245-6aa51d157600
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: DrawDibTime, DrawDibTime function [Windows Multimedia], _win32_DrawDibTime, multimedia.drawdibtime, vfw/DrawDibTime
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
req.product: Windows UI
---

# DrawDibTime function


## -description



The <b>DrawDibTime</b> function retrieves timing information about the drawing operation and is used during debug operations.




## -parameters




### -param hdd


            Handle to a DrawDib DC.
          


### -param lpddtime


            Pointer to a <a href="https://msdn.microsoft.com/ec8a4e04-9e38-4db3-bb2b-838c63284f3a">DRAWDIBTIME</a> structure.
          


## -returns




            Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.
          




## -remarks



This function is present only in the debug version of the Microsoft Windows Software Development Kit (SDK) libraries.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

