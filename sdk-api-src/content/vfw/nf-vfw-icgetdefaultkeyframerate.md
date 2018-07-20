---
UID: NF:vfw.ICGetDefaultKeyFrameRate
title: ICGetDefaultKeyFrameRate macro
author: windows-sdk-content
description: The ICGetDefaultKeyFrameRate macro queries a video compression driver for its default (or preferred) key-frame spacing. You can use this macro or explicitly call the ICM_GETDEFAULTKEYFRAMERATE message.
old-location: multimedia\icgetdefaultkeyframerate.htm
old-project: Multimedia
ms.assetid: 81ae287a-13e3-4bf0-bdd8-915a81e78d32
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: ICGetDefaultKeyFrameRate, ICGetDefaultKeyFrameRate macro [Windows Multimedia], _win32_ICGetDefaultKeyFrameRate, multimedia.icgetdefaultkeyframerate, vfw/ICGetDefaultKeyFrameRate
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
 - ICGetDefaultKeyFrameRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICGetDefaultKeyFrameRate macro


## -description



The <b>ICGetDefaultKeyFrameRate</b> macro queries a video compression driver for its default (or preferred) key-frame spacing. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/2ebe37cc-3ec2-4b52-bd8f-71c44b704647">ICM_GETDEFAULTKEYFRAMERATE</a> message.




## -parameters




### -param hic

Handle to a compressor. 


#### - wParam

Address to contain the preferred key-frame spacing. 


## -remarks



The <b>ICGetDefaultKeyFrameRate</b> macro returns the default key frame rate.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

