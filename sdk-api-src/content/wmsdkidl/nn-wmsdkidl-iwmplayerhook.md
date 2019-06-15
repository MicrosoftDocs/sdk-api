---
UID: NN:wmsdkidl.IWMPlayerHook
title: IWMPlayerHook (wmsdkidl.h)
author: windows-sdk-content
description: The IWMPlayerHook interface can be implemented by a player application that uses DirectX Video Acceleration (DirectX VA).
old-location: wmformat\iwmplayerhook.htm
tech.root: wmformat
ms.assetid: 5e58cb6a-3398-4b12-881e-76f936f6c7b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPlayerHook, IWMPlayerHook interface [windows Media Format], IWMPlayerHook interface [windows Media Format],described, IWMPlayerHookInterface, wmformat.iwmplayerhook, wmsdkidl/IWMPlayerHook
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
 - IWMPlayerHook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPlayerHook interface


## -description



The <b>IWMPlayerHook</b> interface can be implemented by a player application that uses DirectX Video Acceleration (DirectX VA). This interface enables application-specific processing to be performed when samples from a video stream are passed to the DirectX VA enabled video card for decompression.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPlayerHook</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPlayerHook</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPlayerHook</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode">PreDecode</a>
</td>
<td align="left" width="63%">
Callback method that performs application-specific processing when called by the reader.

</td>
</tr>
</table> 


## -remarks



To assign an implementation of the <b>IWMPlayerHook</b> interface to an output in the reader object, call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced5-setplayerhook">IWMReaderAdvanced5::SetPlayerHook</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

