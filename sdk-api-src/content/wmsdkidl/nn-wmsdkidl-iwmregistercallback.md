---
UID: NN:wmsdkidl.IWMRegisterCallback
title: IWMRegisterCallback
author: windows-sdk-content
description: The IWMRegisterCallback interface enables the application to get status messages from a sink object.By default, the writer object does not send the application any status messages from the sink object.
old-location: wmformat\iwmregistercallback.htm
tech.root: wmformat
ms.assetid: 3831b727-7fdc-4d05-a7b3-86ca5b5c3b17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMRegisterCallback, IWMRegisterCallback interface [windows Media Format], IWMRegisterCallback interface [windows Media Format],described, IWMRegisterCallbackInterface, wmformat.iwmregistercallback, wmsdkidl/IWMRegisterCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmsdkidl.h
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
 - wmsdkidl.h
api_name:
 - IWMRegisterCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMRegisterCallback interface


## -description



The <b>IWMRegisterCallback</b> interface enables the application to get status messages from a sink object.

By default, the writer object does not send the application any status messages from the sink object. To get status messages from a sink object, the application must query the sink object for the <b>IWMRegisterCallback</b> interface and call the <b>Advise</b> method.

The file sink object, the network sink object, and the push sink object all expose this interface. To obtain a pointer to this interface for a sink, call <b>QueryInterface</b> on any of these sink objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMRegisterCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMRegisterCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMRegisterCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69d12e5c-23fd-4d4b-959e-fe7979bf3fdb">Advise</a>
</td>
<td align="left" width="63%">
Registers the application to receive status messages from the sink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f320288-09a8-4eaf-a7cd-54a4b52d0b47">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters the application's callback interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/93f44579-fb2d-498e-a271-5bc91d6f0321">Writer File Sink Object</a>



<a href="https://msdn.microsoft.com/f7765b42-693a-4f48-b750-17579e860b6d">Writer Network Sink Object</a>
 

 

