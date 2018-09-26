---
UID: NF:vpconfig.IVPBaseConfig.GetMaxPixelRate
title: IVPBaseConfig::GetMaxPixelRate
author: windows-sdk-content
description: The GetMaxPixelRate method retrieves the maximum pixel rate the device will output for a given width and height.
old-location: dshow\ivpbaseconfig_getmaxpixelrate.htm
tech.root: DirectShow
ms.assetid: 9b86ff2c-c51f-4498-a000-5f1868c2c24b
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetMaxPixelRate, GetMaxPixelRate method [DirectShow], GetMaxPixelRate method [DirectShow],IVPBaseConfig interface, IVPBaseConfig interface [DirectShow],GetMaxPixelRate method, IVPBaseConfig.GetMaxPixelRate, IVPBaseConfig::GetMaxPixelRate, IVPBaseConfigGetMaxPixelRate, dshow.ivpbaseconfig_getmaxpixelrate, vpconfig/IVPBaseConfig::GetMaxPixelRate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vpconfig.h
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
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.GetMaxPixelRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseConfig::GetMaxPixelRate


## -description



The <code>GetMaxPixelRate</code> method retrieves the maximum pixel rate the device will output for a given width and height.




## -parameters




### -param pamvpSize [in, out]

Pointer to an <a href="https://msdn.microsoft.com/e36163bc-a7ea-421e-b876-2d459ecb11e8">AMVPSIZE</a> structure containing the desired width and height.


### -param pdwMaxPixelsPerSecond [out]

Pointer to a variable that receives the maximum pixel rate, in pixels per second.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method retrieves the maximum pixels per second expected for a given size. If the device does not support this size, then it returns the rate and the size that it supports.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 

