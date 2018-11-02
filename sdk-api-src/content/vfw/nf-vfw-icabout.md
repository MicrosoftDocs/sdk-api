---
UID: NF:vfw.ICAbout
title: ICAbout macro
author: windows-sdk-content
description: The ICAbout macro notifies a video compression driver to display its About dialog box. You can use this macro or explicitly call the ICM_ABOUT message.
old-location: multimedia\icabout.htm
tech.root: Multimedia
ms.assetid: 18ec2659-8589-4a13-95ea-825a3aecbf98
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ICAbout, ICAbout macro [Windows Multimedia], _win32_ICAbout, multimedia.icabout, vfw/ICAbout
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
 - ICAbout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICAbout macro


## -description



The <b>ICAbout</b> macro notifies a video compression driver to display its About dialog box. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/6eca69a3-0463-48e6-befb-5003b7515e7d">ICM_ABOUT</a> message.




## -parameters




### -param hic

Handle of the compressor. 


### -param hwnd

Handle of the parent window of the displayed dialog box.

You can also determine if a driver has an About dialog box by specifying -1 in this parameter, as in the <a href="https://msdn.microsoft.com/073f217f-961b-4de2-9430-5ee81379e807">ICQueryAbout</a> macro. The driver returns ICERR_OK if it has an About dialog box or ICERR_UNSUPPORTED otherwise.


## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

