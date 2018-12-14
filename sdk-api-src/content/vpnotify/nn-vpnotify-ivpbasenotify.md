---
UID: NN:vpnotify.IVPBaseNotify
title: IVPBaseNotify
author: windows-sdk-content
description: Enables the Overlay Mixer to control the properties of a hardware device such as a decoder that uses a video port. The IVPNotify interface derives from this interface.Applications should never use this interface.
old-location: dshow\ivpbasenotify.htm
tech.root: DirectShow
ms.assetid: c72bd662-366c-4102-9ad9-9e4c59096ede
ms.author: windowssdkdev
ms.date: 12/5/2018
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
 - IVPBaseNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseNotify interface


## -description



Enables the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> to control the properties of a hardware device such as a decoder that uses a video port. The <a href="https://msdn.microsoft.com/en-us/library/Dd390589(v=VS.85).aspx">IVPNotify</a> interface derives from this interface.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd390582(v=VS.85).aspx">RenegotiateVPParameters</a>
</td>
<td align="left" width="63%">
Initializes the connection to the decoder.

</td>
</tr>
</table> 


## -remarks



Include Vptype.h before Vpnotify.h.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd390567(v=VS.85).aspx">IVPBaseConfig</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390583(v=VS.85).aspx">IVPConfig</a>
 

 

