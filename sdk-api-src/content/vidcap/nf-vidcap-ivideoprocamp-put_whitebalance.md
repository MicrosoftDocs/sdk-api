---
UID: NF:vidcap.IVideoProcAmp.put_WhiteBalance
title: IVideoProcAmp::put_WhiteBalance
author: windows-sdk-content
description: The put_WhiteBalance method sets the camera's white balance, specified as a color temperature.
old-location: dshow\ivideoprocamp_put_whitebalance.htm
tech.root: DirectShow
ms.assetid: b79e64e1-4b0f-4111-ae25-54891f743c01
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_WhiteBalance method, IVideoProcAmp.put_WhiteBalance, IVideoProcAmp::put_WhiteBalance, IVideoProcAmpput_WhiteBalance, dshow.ivideoprocamp_put_whitebalance, put_WhiteBalance, put_WhiteBalance method [DirectShow], put_WhiteBalance method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_WhiteBalance
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVideoProcAmp.put_WhiteBalance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::put_WhiteBalance


## -description


The <code>put_WhiteBalance</code> method sets the camera's white balance, specified as a color temperature.


## -parameters




### -param Value [in]

Specifies the white balance, in degrees Kelvin.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

