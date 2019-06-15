---
UID: NF:strmif.IQualityControl.Notify
title: IQualityControl::Notify (strmif.h)
author: windows-sdk-content
description: The Notify method notifies the filter that a quality change is requested.
old-location: dshow\iqualitycontrol_notify.htm
tech.root: DirectShow
ms.assetid: c7a34356-b0b2-49c1-bdc2-d8043fdc2862
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IQualityControl interface [DirectShow],Notify method, IQualityControl.Notify, IQualityControl::Notify, IQualityControlNotify, Notify, Notify method [DirectShow], Notify method [DirectShow],IQualityControl interface, dshow.iqualitycontrol_notify, strmif/IQualityControl::Notify
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
ms.custom: 19H1
---

# IQualityControl::Notify


## -description



The <code>Notify</code> method notifies the filter that a quality change is requested.




## -parameters




### -param pSelf [in]

Pointer to the filter that is sending the quality notification.


### -param q [in]


<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-tagquality">Quality</a> structure.


## -returns



Returns S_OK if the method succeeds; otherwise, returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iqualitycontrol">IQualityControl Interface</a>
 

 

