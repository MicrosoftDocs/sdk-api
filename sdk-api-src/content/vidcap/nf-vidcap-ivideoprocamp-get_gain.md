---
UID: NF:vidcap.IVideoProcAmp.get_Gain
title: IVideoProcAmp::get_Gain (vidcap.h)
author: windows-sdk-content
description: The get_Gain method returns the camera's gain setting.
old-location: dshow\ivideoprocamp_get_gain.htm
tech.root: DirectShow
ms.assetid: 36d84db9-4a53-4087-b389-e707ed3d5572
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Gain method, IVideoProcAmp.get_Gain, IVideoProcAmp::get_Gain, IVideoProcAmpget_Gain, dshow.ivideoprocamp_get_gain, get_Gain, get_Gain method [DirectShow], get_Gain method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Gain
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
 - IVideoProcAmp.get_Gain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::get_Gain


## -description


The <code>get_Gain</code> method returns the camera's gain setting.


## -parameters




### -param pValue [out]

Receives the gain setting. Larger values indicate higher gain.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd407327(v=VS.85).aspx">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377236(v=VS.85).aspx">IVideoProcAmp Interface</a>
 

 

