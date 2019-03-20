---
UID: NF:vidcap.IVideoProcAmp.put_Sharpness
title: IVideoProcAmp::put_Sharpness (vidcap.h)
author: windows-sdk-content
description: The put_Sharpness method sets the camera's sharpness setting.
old-location: dshow\ivideoprocamp_put_sharpness.htm
tech.root: DirectShow
ms.assetid: a47e8f21-29ec-4845-97b2-1a9d6478afa6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_Sharpness method, IVideoProcAmp.put_Sharpness, IVideoProcAmp::put_Sharpness, IVideoProcAmpput_Sharpness, dshow.ivideoprocamp_put_sharpness, put_Sharpness, put_Sharpness method [DirectShow], put_Sharpness method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Sharpness
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - Vidcap.h
api_name:
 - IVideoProcAmp.put_Sharpness
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::put_Sharpness


## -description


The <code>put_Sharpness</code> method sets the camera's sharpness setting.


## -parameters




### -param Value [in]

Specifies the sharpness setting. Larger values indicate increasing sharpness.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd407327(v=VS.85).aspx">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377236(v=VS.85).aspx">IVideoProcAmp Interface</a>
 

 

