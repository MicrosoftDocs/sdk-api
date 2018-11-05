---
UID: NF:vfw.ICGetDefaultQuality
title: ICGetDefaultQuality macro
author: windows-sdk-content
description: The ICGetDefaultQuality macro queries a video compression driver to provide its default quality setting. You can use this macro or explicitly call the ICM_GETDEFAULTQUALITY message.
old-location: multimedia\icgetdefaultquality.htm
tech.root: Multimedia
ms.assetid: dd88a141-5461-4725-83f9-c2ead3a3a2b6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICGetDefaultQuality, ICGetDefaultQuality macro [Windows Multimedia], _win32_ICGetDefaultQuality, multimedia.icgetdefaultquality, vfw/ICGetDefaultQuality
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
 - ICGetDefaultQuality
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICGetDefaultQuality macro


## -description



The <b>ICGetDefaultQuality</b> macro queries a video compression driver to provide its default quality setting. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/bba7f451-52c2-4684-a7c9-e4b05cb946c5">ICM_GETDEFAULTQUALITY</a> message.




## -parameters




### -param hic

Handle to a compressor. 


#### - wParam

Address to contain the default quality value. Quality values range from 0 to 10,000. 


## -remarks



The <b>ICGetDefaultQuality</b> macro returns the default quality value.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

