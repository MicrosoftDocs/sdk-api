---
UID: NF:vpconfig.IVPBaseConfig.SetVideoFormat
title: IVPBaseConfig::SetVideoFormat
author: windows-sdk-content
description: The SetVideoFormat method sets the video format.
old-location: dshow\ivpbaseconfig_setvideoformat.htm
tech.root: DirectShow
ms.assetid: 98b4182f-c286-4f4a-86b8-40d093456628
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetVideoFormat method, IVPBaseConfig.SetVideoFormat, IVPBaseConfig::SetVideoFormat, IVPBaseConfigSetVideoFormat, SetVideoFormat, SetVideoFormat method [DirectShow], SetVideoFormat method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setvideoformat, vpconfig/IVPBaseConfig::SetVideoFormat
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
 - IVPBaseConfig.SetVideoFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseConfig::SetVideoFormat


## -description



The <code>SetVideoFormat</code> method sets the video format.




## -parameters




### -param dwChosenEntry [in]

Value specifying the index (zero-based) of the video pixel format to use.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Retrieve the video formats by using <a href="https://msdn.microsoft.com/a0426a2a-a856-4e5d-8ff2-4afa3b18355e">IVPBaseConfig::GetVideoFormats</a>.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 

