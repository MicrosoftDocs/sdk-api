---
UID: NF:amvideo.IQualProp.get_Jitter
title: IQualProp::get_Jitter
author: windows-sdk-content
description: The get_Jitter method gets the jitter (variation in time) between successive frames delivered to the video renderer.
old-location: dshow\iqualprop_get_jitter.htm
tech.root: DirectShow
ms.assetid: e1f6e93f-58d6-41b4-b16f-e9f02bfec0fe
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IQualProp interface [DirectShow],get_Jitter method, IQualProp.get_Jitter, IQualProp::get_Jitter, IQualPropget_Jitter, amvideo/IQualProp::get_Jitter, dshow.iqualprop_get_jitter, get_Jitter, get_Jitter method [DirectShow], get_Jitter method [DirectShow],IQualProp interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amvideo.h
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
 - IQualProp.get_Jitter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQualProp::get_Jitter


## -description


The <b>get_Jitter</b> method gets the jitter (variation in time) between successive frames delivered to the video renderer.


## -parameters




### -param iJitter

TBD




#### - piJitter

Receives the standard deviation of the interframe time, in milliseconds.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/428dfb97-0dfa-442c-819e-291e6a58f712">IQualProp Interface</a>
 

 

