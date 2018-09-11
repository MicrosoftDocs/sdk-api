---
UID: NF:mpconfig.IMixerPinConfig.SetZOrder
title: IMixerPinConfig::SetZOrder
author: windows-sdk-content
description: The SetZOrder method sets the z-order of a particular video stream.
old-location: dshow\imixerpinconfig_setzorder.htm
tech.root: DirectShow
ms.assetid: fe8e71b8-9aaf-438e-b370-5ba9f131bf7a
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IMixerPinConfig interface [DirectShow],SetZOrder method, IMixerPinConfig.SetZOrder, IMixerPinConfig::SetZOrder, IMixerPinConfigSetZOrder, SetZOrder, SetZOrder method [DirectShow], SetZOrder method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setzorder, mpconfig/IMixerPinConfig::SetZOrder
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
 - IMixerPinConfig.SetZOrder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMixerPinConfig::SetZOrder


## -description



The <code>SetZOrder</code> method sets the z-order of a particular video stream.



This method is not currently implemented and returns E_NOTIMPL.


## -parameters




### -param dwZOrder [in]

Value indicating the order in which streams will clip each other.


## -returns



Returns E_NOTIMPL.




## -remarks



The z-order indicates which streams can clip other streams. Images with larger z-values are always in front of images with smaller z-values.

The relative order of multiple streams is significant only if the video images overlap.

Specifying the same z-order for two overlapping streams can cause strange video artifacts.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/5089a2b3-2973-4761-82f6-f6af3ac9f560">IMixerPinConfig::GetZOrder</a>
 

 

