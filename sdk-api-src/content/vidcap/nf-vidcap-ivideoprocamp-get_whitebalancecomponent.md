---
UID: NF:vidcap.IVideoProcAmp.get_WhiteBalanceComponent
title: IVideoProcAmp::get_WhiteBalanceComponent (vidcap.h)
author: windows-sdk-content
description: The get_WhiteBalanceComponent method returns the camera's white balance, specified as red and blue component values.
old-location: dshow\ivideoprocamp_get_whitebalancecomponent.htm
tech.root: DirectShow
ms.assetid: b9beb89f-df55-4b76-a679-5e27cb0af9fb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_WhiteBalanceComponent method, IVideoProcAmp.get_WhiteBalanceComponent, IVideoProcAmp::get_WhiteBalanceComponent, IVideoProcAmpget_WhiteBalanceComponent, dshow.ivideoprocamp_get_whitebalancecomponent, get_WhiteBalanceComponent, get_WhiteBalanceComponent method [DirectShow], get_WhiteBalanceComponent method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_WhiteBalanceComponent
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
 - IVideoProcAmp.get_WhiteBalanceComponent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::get_WhiteBalanceComponent


## -description


The <code>get_WhiteBalanceComponent</code> method returns the camera's white balance, specified as red and blue component values.


## -parameters




### -param pValue1 [out]

Receives the red component.


### -param pValue2 [out]

Receives the blue component.


### -param pFlags [in, out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd407327(v=VS.85).aspx">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377236(v=VS.85).aspx">IVideoProcAmp Interface</a>
 

 

