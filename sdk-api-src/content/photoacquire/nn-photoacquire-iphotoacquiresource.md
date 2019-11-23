---
UID: NN:photoacquire.IPhotoAcquireSource
title: IPhotoAcquireSource (photoacquire.h)

description: The IPhotoAcquireSource interface is used for acquisition of items from a device.
old-location: picacq\iphotoacquiresource.htm
tech.root: acquisition
ms.assetid: 6671d550-8c12-40e3-bf6f-33203e69cff0

ms.date: 12/05/2018
ms.keywords: IPhotoAcquireSource, IPhotoAcquireSource interface [Picture Acquisition], IPhotoAcquireSource interface [Picture Acquisition],described, IPhotoAcquireSourceInterface, photoacquire/IPhotoAcquireSource, picacq.iphotoacquiresource
ms.topic: interface
f1_keywords: 
 - "photoacquire/IPhotoAcquireSource"
dev_langs:
 - c++
req.header: photoacquire.h
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
 - photoacquire.h
api_name:
 - IPhotoAcquireSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquireSource interface


## -description



The <code>IPhotoAcquireSource</code> interface is used for acquisition of items from a device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireSource</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhotoAcquireSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoAcquireSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-getdeviceicons">GetDeviceIcons</a>
</td>
<td align="left" width="63%">
Retrieves the icons that are used to represent the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-getdeviceid">GetDeviceId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier (ID) of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-getfriendlyname">GetFriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device, formatted for display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-getitemat">GetItemAt</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem</a> object at the given index in the list of items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-getitemcount">GetItemCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items found by the <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-initializeitemlist">InitializeItemList</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-getphotoacquiresettings">GetPhotoAcquireSettings</a>
</td>
<td align="left" width="63%">
Obtains an <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings</a> object for working with acquisition settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-initializeitemlist">InitializeItemList</a>
</td>
<td align="left" width="63%">
Enumerates transferable items on the device and passes each item to the optional progress callback, if it is supplied.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/interfaces">Interfaces</a>
 

 

