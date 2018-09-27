---
UID: NF:strmif.IQualityControl.Notify
title: IQualityControl::Notify
author: windows-sdk-content
description: The Notify method notifies the filter that a quality change is requested.
old-location: dshow\iqualitycontrol_notify.htm
tech.root: DirectShow
ms.assetid: c7a34356-b0b2-49c1-bdc2-d8043fdc2862
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IQualityControl interface [DirectShow],Notify method, IQualityControl.Notify, IQualityControl::Notify, IQualityControlNotify, Notify, Notify method [DirectShow], Notify method [DirectShow],IQualityControl interface, dshow.iqualitycontrol_notify, strmif/IQualityControl::Notify
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
 - IQualityControl.Notify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQualityControl::Notify


## -description



The <code>Notify</code> method notifies the filter that a quality change is requested.




## -parameters




### -param pSelf [in]

Pointer to the filter that is sending the quality notification.


### -param q [in]


<a href="https://msdn.microsoft.com/2ab7fcde-0e44-4d60-acf5-3638efbe15f7">Quality</a> structure.


## -returns



Returns S_OK if the method succeeds; otherwise, returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2672e563-75d7-4a8a-b914-7b0712e856e8">IQualityControl Interface</a>
 

 

