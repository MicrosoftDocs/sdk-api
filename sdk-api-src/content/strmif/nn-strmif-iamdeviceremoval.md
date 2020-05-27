---
UID: NN:strmif.IAMDeviceRemoval
title: IAMDeviceRemoval (strmif.h)
description: The IAMDeviceRemoval interface provides a way for the Filter Graph Manager to register for device removal events for a capture device.
helpviewer_keywords: ["IAMDeviceRemoval","IAMDeviceRemoval interface [DirectShow]","IAMDeviceRemoval interface [DirectShow]","described","IAMDeviceRemovalInterface","dshow.iamdeviceremoval","strmif/IAMDeviceRemoval"]
old-location: dshow\iamdeviceremoval.htm
tech.root: DirectShow
ms.assetid: 3d67f577-9d85-47ca-b887-f259e9acc964
ms.date: 12/05/2018
ms.keywords: IAMDeviceRemoval, IAMDeviceRemoval interface [DirectShow], IAMDeviceRemoval interface [DirectShow],described, IAMDeviceRemovalInterface, dshow.iamdeviceremoval, strmif/IAMDeviceRemoval
f1_keywords:
- strmif/IAMDeviceRemoval
dev_langs:
- c++
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
- IAMDeviceRemoval
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDeviceRemoval interface


## -description



The <code>IAMDeviceRemoval</code> interface provides a way for the Filter Graph Manager to register for device removal events for a capture device. The KsProxy filter exposes this interface. (See <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a>.)

Applications typically do not use this interface, and third-party filters do not need to implement this interface. To get a pointer to this interface, call <b>QueryInterface</b> on the KsProxy filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMDeviceRemoval</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDeviceRemoval</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMDeviceRemoval</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdeviceremoval-deviceinfo">DeviceInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the device

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdeviceremoval-disassociate">Disassociate</a>
</td>
<td align="left" width="63%">
Disassociates the KsProxy filter from the device by closing the device handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdeviceremoval-reassociate">Reassociate</a>
</td>
<td align="left" width="63%">
Reassociates the KsProxy filter with the device.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

