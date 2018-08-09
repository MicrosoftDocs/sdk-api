---
UID: NF:vfw.ICGetStateSize
title: ICGetStateSize macro
author: windows-sdk-content
description: The ICGetStateSize macro queries a video compression driver to determine the amount of memory required to retrieve the configuration information. You can use this macro or explicitly call the ICM_GETSTATE message.
old-location: multimedia\icgetstatesize.htm
old-project: Multimedia
ms.assetid: 386761e8-9234-4541-b593-ce8e323714bf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICGetStateSize, ICGetStateSize macro [Windows Multimedia], _win32_ICGetStateSize, multimedia.icgetstatesize, vfw/ICGetStateSize
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
 - ICGetStateSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICGetStateSize macro


## -description



The <b>ICGetStateSize</b> macro queries a video compression driver to determine the amount of memory required to retrieve the configuration information. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/4b77e294-f3aa-45f9-a4f4-f103b83eae8d">ICM_GETSTATE</a> message.




## -parameters




### -param hic

Handle of the compressor. 


## -remarks



The structure used to represent configuration information is driver specific and is defined by the driver.

Use <b>ICGetStateSize</b> before calling the <a href="https://msdn.microsoft.com/e0066cc2-a67d-4cf4-9d22-506cc152ec14">ICGetState</a> macro to determine the size of buffer to allocate for the call.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

