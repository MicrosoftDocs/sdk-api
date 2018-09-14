---
UID: NF:mpconfig.IMixerPinConfig.GetZOrder
title: IMixerPinConfig::GetZOrder
author: windows-sdk-content
description: The GetZOrder method retrieves the z-order of a particular video stream.
old-location: dshow\imixerpinconfig_getzorder.htm
tech.root: DirectShow
ms.assetid: 5089a2b3-2973-4761-82f6-f6af3ac9f560
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetZOrder, GetZOrder method [DirectShow], GetZOrder method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetZOrder method, IMixerPinConfig.GetZOrder, IMixerPinConfig::GetZOrder, IMixerPinConfigGetZOrder, dshow.imixerpinconfig_getzorder, mpconfig/IMixerPinConfig::GetZOrder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mpconfig.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerPinConfig.GetZOrder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMixerPinConfig::GetZOrder


## -description



The <code>GetZOrder</code> method retrieves the z-order of a particular video stream.



This method is not currently implemented and returns E_NOTIMPL.


## -parameters




### -param pdwZOrder [out]

Pointer to a value indicating the order in which streams will clip each other.


## -returns



Returns E_NOTIMPL.




## -remarks



Images with larger z-values are always in front of images with smaller z-values.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/fe8e71b8-9aaf-438e-b370-5ba9f131bf7a">IMixerPinConfig::SetZOrder</a>
 

 

