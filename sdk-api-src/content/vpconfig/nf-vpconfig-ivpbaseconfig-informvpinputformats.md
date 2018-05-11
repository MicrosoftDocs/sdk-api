---
UID: NF:vpconfig.IVPBaseConfig.InformVPInputFormats
title: IVPBaseConfig::InformVPInputFormats
author: windows-driver-content
description: The InformVPInputFormats method informs the device what video formats the video port supports.
old-location: dshow\ivpbaseconfig_informvpinputformats.htm
old-project: DirectShow
ms.assetid: d9b4ea2b-ad71-4226-9aad-e68a9cb26274
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IVPBaseConfig interface [DirectShow],InformVPInputFormats method, IVPBaseConfig.InformVPInputFormats, IVPBaseConfig::InformVPInputFormats, IVPBaseConfigInformVPInputFormats, InformVPInputFormats, InformVPInputFormats method [DirectShow], InformVPInputFormats method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_informvpinputformats, vpconfig/IVPBaseConfig::InformVPInputFormats
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
req.typenames: VMR9VideoStreamInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vpconfig.h
api_name:
-	IVPBaseConfig.InformVPInputFormats
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVPBaseConfig::InformVPInputFormats


## -description



The <code>InformVPInputFormats</code> method informs the device what video formats the video port supports.




## -parameters




### -param dwNumFormats [in]

Number of video formats contained in the <i>pDDPixelFormats</i> parameter.


### -param pDDPixelFormats [in]

Pointer to an array of pixel format structures (<b>DDPIXELFORMAT</b>) to send to the device.


## -returns



Returns S_FALSE if failure, or S_OK otherwise.




## -remarks



The supplied array of supported video port formats might determine what formats the device, in turn, proposes.

The <b>DDPIXELFORMAT</b> structure is documented in the Windows DDK.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 

