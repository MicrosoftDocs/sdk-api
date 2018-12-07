---
UID: NF:vpconfig.IVPConfig.IsVPDecimationAllowed
title: IVPConfig::IsVPDecimationAllowed
author: windows-sdk-content
description: The IsVPDecimationAllowed method, given the context, retrieves whether scaling at the video port is possible.
old-location: dshow\ivpconfig_isvpdecimationallowed.htm
tech.root: DirectShow
ms.assetid: 2362e321-cbdd-41ee-97ff-e6ff9cd672b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVPConfig interface [DirectShow],IsVPDecimationAllowed method, IVPConfig.IsVPDecimationAllowed, IVPConfig::IsVPDecimationAllowed, IVPConfigIsVPDecimationAllowed, IsVPDecimationAllowed, IsVPDecimationAllowed method [DirectShow], IsVPDecimationAllowed method [DirectShow],IVPConfig interface, dshow.ivpconfig_isvpdecimationallowed, vpconfig/IVPConfig::IsVPDecimationAllowed
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
 - IVPConfig.IsVPDecimationAllowed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPConfig::IsVPDecimationAllowed


## -description



The <code>IsVPDecimationAllowed</code> method, given the context, retrieves whether scaling at the video port is possible.




## -parameters




### -param pbIsDecimationAllowed [out]

Receives a Boolean value indicating whether decimation is possible.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter uses this function to determine whether the driver needs the mixer to decimate video data at its own discretion. This function can be especially useful in a capture with preview situation in which you would not want the VP mixer filter to perform any scaling at the video port.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2c0eb294-7e57-4d8d-98b1-57c3834279a0">IVPConfig Interface</a>
 

 

