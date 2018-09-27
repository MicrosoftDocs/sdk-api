---
UID: NF:dshowasf.IAMWMBufferPassCallback.Notify
title: IAMWMBufferPassCallback::Notify
author: windows-sdk-content
description: The Notify method is called by the pin for each buffer that is delivered during streaming.
old-location: wmformat\iamwmbufferpasscallback_notify.htm
tech.root: wmformat
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAMWMBufferPassCallback interface [windows Media Format],Notify method, IAMWMBufferPassCallback.Notify, IAMWMBufferPassCallback::Notify, IAMWMBufferPassCallbackNotify, Notify, Notify method [windows Media Format], Notify method [windows Media Format],IAMWMBufferPassCallback interface, dshowasf/IAMWMBufferPassCallback::Notify, wmformat.iamwmbufferpasscallback_notify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - dshowasf.h
api_name:
 - IAMWMBufferPassCallback.Notify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMWMBufferPassCallback::Notify


## -description



The <b>Notify</b> method is called by the pin for each buffer that is delivered during streaming.




## -parameters




### -param pNSSBuffer3 [in]

Pointer to the <a href="https://msdn.microsoft.com/3ebf80d0-b5b0-4024-805d-e0a3855574bf">INSSBuffer3</a> interface exposed on the media sample.


### -param pPin [in]

Pointer to the pin associated with the media stream that the sample belongs to.


### -param prtStart [in]

Start time of the sample.


### -param prtEnd [in]

End time of the sample.


## -returns



No particular return value is specified. The calling pin ignores the <b>HRESULT</b>.




## -remarks



This method enables an application to examine and act on information in the media buffer before the buffer contents are processed. The application is responsible for knowing the media type on the pin. This information can be obtained by first getting the stream information from the profile and then calling <a href="https://msdn.microsoft.com/f645a742-e6dc-4041-8a56-3bbb5188a9a9">IConfigAsfWriter2::StreamNumFromPin</a> method to determine which pin is associated with each stream.




## -see-also




<a href="https://msdn.microsoft.com/66f483b5-3886-48b4-bc43-7c3517abd20d">DirectShow QASF Reference</a>



<a href="https://msdn.microsoft.com/5bf0ae2e-504b-471b-bfc9-aa48f534e03f">IAMWMBufferPassCallback Interface</a>



<a href="https://msdn.microsoft.com/3ebf80d0-b5b0-4024-805d-e0a3855574bf">INSSBuffer3 Interface</a>
 

 

