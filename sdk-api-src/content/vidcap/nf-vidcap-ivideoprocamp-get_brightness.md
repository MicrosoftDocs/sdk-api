---
UID: NF:vidcap.IVideoProcAmp.get_Brightness
title: IVideoProcAmp::get_Brightness
author: windows-sdk-content
description: The get_Brightness method returns the camera's brightness setting.
old-location: dshow\ivideoprocamp_get_brightness.htm
tech.root: DirectShow
ms.assetid: b0e3b7cf-c133-4b47-8209-1014d1e3d671
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Brightness method, IVideoProcAmp.get_Brightness, IVideoProcAmp::get_Brightness, IVideoProcAmpget_Brightness, dshow.ivideoprocamp_get_brightness, get_Brightness, get_Brightness method [DirectShow], get_Brightness method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Brightness
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
 - IVideoProcAmp.get_Brightness
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::get_Brightness


## -description


The <code>get_Brightness</code> method returns the camera's brightness setting.


## -parameters




### -param pValue [out]

Receives the brightness setting. Larger values indicate increased brightness.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd407327(v=VS.85).aspx">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377236(v=VS.85).aspx">IVideoProcAmp Interface</a>
 

 

