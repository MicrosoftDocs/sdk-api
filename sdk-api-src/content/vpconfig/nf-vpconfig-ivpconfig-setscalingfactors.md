---
UID: NF:vpconfig.IVPConfig.SetScalingFactors
title: IVPConfig::SetScalingFactors
author: windows-sdk-content
description: The SetScalingFactors method sets the factors by which the decoder should scale the video stream.
old-location: dshow\ivpconfig_setscalingfactors.htm
old-project: DirectShow
ms.assetid: 62b8281e-6feb-43f5-b1a5-36444fda5543
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IVPConfig interface [DirectShow],SetScalingFactors method, IVPConfig.SetScalingFactors, IVPConfig::SetScalingFactors, IVPConfigSetScalingFactors, SetScalingFactors, SetScalingFactors method [DirectShow], SetScalingFactors method [DirectShow],IVPConfig interface, dshow.ivpconfig_setscalingfactors, vpconfig/IVPConfig::SetScalingFactors
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vpconfig.h
req.include-header: 
req.redist: 
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
req.typenames: VMR9VideoStreamInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVPConfig.SetScalingFactors
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVPConfig::SetScalingFactors


## -description



The <code>SetScalingFactors</code> method sets the factors by which the decoder should scale the video stream.




## -parameters




### -param pamvpSize [in]

Pointer to the new scaling size structure (<a href="https://msdn.microsoft.com/e36163bc-a7ea-421e-b876-2d459ecb11e8">AMVPSIZE</a>) to use to specify the width and height.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If the decoder does not support the specified scaling factors, then it sets the values to the nearest factors it can support.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2c0eb294-7e57-4d8d-98b1-57c3834279a0">IVPConfig Interface</a>
 

 

