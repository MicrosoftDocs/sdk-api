---
UID: NF:vpnotify.IVPBaseNotify.RenegotiateVPParameters
title: IVPBaseNotify::RenegotiateVPParameters
author: windows-sdk-content
description: The RenegotiateVPParameters method initializes the connection to the decoder.
old-location: dshow\ivpbasenotify_renegotiatevpparameters.htm
tech.root: DirectShow
ms.assetid: b35a0e8f-3d4f-443d-b76c-83b44745a86d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IVPBaseNotify interface [DirectShow],RenegotiateVPParameters method, IVPBaseNotify.RenegotiateVPParameters, IVPBaseNotify::RenegotiateVPParameters, IVPBaseNotifyRenegotiateVPParameters, RenegotiateVPParameters, RenegotiateVPParameters method [DirectShow], RenegotiateVPParameters method [DirectShow],IVPBaseNotify interface, dshow.ivpbasenotify_renegotiatevpparameters, vpnotify/IVPBaseNotify::RenegotiateVPParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vpnotify.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpnotify.h
api_name:
 - IVPBaseNotify.RenegotiateVPParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseNotify::RenegotiateVPParameters


## -description



The <code>RenegotiateVPParameters</code> method initializes the connection to the decoder.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter negotiates various parameters (by using the <a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig</a> interface) with the decoder or driver. Call this method if any of those parameters (such as the video format or size) change. Currently, the Overlay Mixer repeats the whole connection process. You can call this method even while the graph is playing.

Include Vptype.h before Vpnotify.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c72bd662-366c-4102-9ad9-9e4c59096ede">IVPBaseNotify Interface</a>
 

 

