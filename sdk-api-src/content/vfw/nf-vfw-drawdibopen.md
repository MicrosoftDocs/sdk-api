---
UID: NF:vfw.DrawDibOpen
title: DrawDibOpen function
author: windows-sdk-content
description: The DrawDibOpen function opens the DrawDib library for use and creates a DrawDib DC for drawing.
old-location: multimedia\drawdibopen.htm
tech.root: Multimedia
ms.assetid: bf0f0c56-df07-455e-9e00-38dc94ababb3
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: DrawDibOpen, DrawDibOpen function [Windows Multimedia], _win32_DrawDibOpen, multimedia.drawdibopen, vfw/DrawDibOpen
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
 - DrawDibOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DrawDibOpen
: 
---

# DrawDibOpen function


## -description



The <b>DrawDibOpen</b> function opens the DrawDib library for use and creates a DrawDib DC for drawing.




## -parameters






## -returns



Returns a handle to a DrawDib DC if successful or <b>NULL</b> otherwise.




## -remarks



When drawing multiple DIBs simultaneously, create a DrawDib DC for each of the images that will be simultaneously on-screen.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

