---
UID: NF:dshowasf.IAMWMBufferPassCallback.Notify
title: IAMWMBufferPassCallback::Notify
author: windows-sdk-content
description: The Notify method is called by the pin for each buffer that is delivered during streaming.
old-location: dshow\iamwmbufferpasscallback_notify.htm
old-project: DirectShow
ms.assetid: 13778b61-0e75-412f-b1e4-eaaf5ec0c853
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMWMBufferPassCallback interface [DirectShow],Notify method, IAMWMBufferPassCallback.Notify, IAMWMBufferPassCallback::Notify, IAMWMBufferPassCallbackNotify, Notify, Notify method [DirectShow], Notify method [DirectShow],IAMWMBufferPassCallback interface, dshow.iamwmbufferpasscallback_notify, dshowasf/IAMWMBufferPassCallback::Notify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dshowasf.h
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dshowasf.h
api_name:
-	IAMWMBufferPassCallback.Notify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAMWMBufferPassCallback::Notify


## -description



The <code>Notify</code> method is called by the pin for each buffer that is delivered during streaming.




## -parameters




### -param pNSSBuffer3 [in]

Pointer to the <a href="https://msdn.microsoft.com/3ebf80d0-b5b0-4024-805d-e0a3855574bf">INSSBuffer3</a> interface of the media sample.


### -param pPin [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of the pin that has delivered or received the sample.


### -param prtStart [in]

Start time of the sample, in 100-nanosecond units.


### -param prtEnd [in]

End time of the sample, in 100-nanosecond units.


## -returns



No particular return value is specified. The calling pin ignores the <b>HRESULT</b>.




## -remarks



This method enables an application to examine and act on information in the media buffer before the buffer contents are processed. The application is responsible for knowing the media type on the pin. This information can be obtained by first getting the stream information from the profile and then calling <a href="https://msdn.microsoft.com/374331ec-6665-4ed9-b4ee-6d33b1e2ef2c">IConfigAsfWriter2::StreamNumFromPin</a> method to determine which pin is associated with each stream. Alternatively, you can call <a href="https://msdn.microsoft.com/f372bfa7-b0ba-43f9-ba86-cbca5d1de515">IPin::ConnectionMediaType</a> on the pin.




## -see-also




<a href="https://msdn.microsoft.com/c3a8e01e-a626-4e47-ad98-e22d1fe88906">IAMWMBufferPassCallback Interface</a>



<a href="https://msdn.microsoft.com/2fae0504-d1da-413a-80dd-de7818f506ef">Using Windows Media in DirectShow</a>
 

 

