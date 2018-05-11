---
UID: NN:vpnotify.IVPBaseNotify
title: IVPBaseNotify
author: windows-driver-content
description: Enables the Overlay Mixer to control the properties of a hardware device such as a decoder that uses a video port. The IVPNotify interface derives from this interface.Applications should never use this interface.
old-location: dshow\ivpbasenotify.htm
old-project: DirectShow
ms.assetid: c72bd662-366c-4102-9ad9-9e4c59096ede
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IVPBaseNotify, IVPBaseNotify interface [DirectShow], IVPBaseNotify interface [DirectShow],described, IVPBaseNotifyInterface, dshow.ivpbasenotify, vpnotify/IVPBaseNotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: VMR9VideoStreamInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vpnotify.h
api_name:
-	IVPBaseNotify
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVPBaseNotify interface


## -description



Enables the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> to control the properties of a hardware device such as a decoder that uses a video port. The <a href="https://msdn.microsoft.com/6b40ba9e-8562-4d31-beaf-e4d4858bf145">IVPNotify</a> interface derives from this interface.

Applications should never use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPBaseNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVPBaseNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPBaseNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b35a0e8f-3d4f-443d-b76c-83b44745a86d">RenegotiateVPParameters</a>
</td>
<td align="left" width="63%">
Initializes the connection to the decoder.

</td>
</tr>
</table> 


## -remarks



Include Vptype.h before Vpnotify.h.




## -see-also




<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig</a>



<a href="https://msdn.microsoft.com/2c0eb294-7e57-4d8d-98b1-57c3834279a0">IVPConfig</a>
 

 

