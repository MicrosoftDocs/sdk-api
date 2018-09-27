---
UID: NF:strmif.IAMVideoProcAmp.Get
title: IAMVideoProcAmp::Get
author: windows-sdk-content
description: The Get method gets the current setting of a video property.
old-location: dshow\iamvideoprocamp_get.htm
tech.root: DirectShow
ms.assetid: 8924383e-23e1-4732-9eff-dc7c8d0e361a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Get, Get method [DirectShow], Get method [DirectShow],IAMVideoProcAmp interface, IAMVideoProcAmp interface [DirectShow],Get method, IAMVideoProcAmp.Get, IAMVideoProcAmp::Get, IAMVideoProcAmpGet, dshow.iamvideoprocamp_get, strmif/IAMVideoProcAmp::Get
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMVideoProcAmp.Get
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoProcAmp::Get


## -description



The <code>Get</code> method gets the current setting of a video property.




## -parameters




### -param Property [in]

Specifies the property to retrieve, as a value from the <a href="https://msdn.microsoft.com/113e3896-4920-41a3-9ce2-a26c34af4896">VideoProcAmpProperty</a> enumeration.
          


### -param lValue [out]

Receives the value of the property.
          


### -param Flags [out]

Receives a member of the <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a> enumeration. The returned value indicates whether the setting is controlled manually or automatically.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f789db78-292e-4092-a5dc-1906845fb1dd">Configure the Video Quality</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/28c45790-2e5a-4acb-8a53-93f19c51dc6a">IAMVideoProcAmp Interface</a>



<a href="https://msdn.microsoft.com/18826377-ddf7-4c36-8995-43310ea077dd">IAMVideoProcAmp::Set</a>
 

 

