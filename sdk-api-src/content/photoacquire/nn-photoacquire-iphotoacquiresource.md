---
UID: NN:photoacquire.IPhotoAcquireSource
title: IPhotoAcquireSource
author: windows-sdk-content
description: The IPhotoAcquireSource interface is used for acquisition of items from a device.
old-location: picacq\iphotoacquiresource.htm
old-project: acquisition
ms.assetid: 6671d550-8c12-40e3-bf6f-33203e69cff0
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IPhotoAcquireSource, IPhotoAcquireSource interface [Picture Acquisition], IPhotoAcquireSource interface [Picture Acquisition],described, IPhotoAcquireSourceInterface, photoacquire/IPhotoAcquireSource, picacq.iphotoacquiresource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - photoacquire.h
api_name:
 - IPhotoAcquireSource
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPhotoAcquireSource interface


## -description



The <code>IPhotoAcquireSource</code> interface is used for acquisition of items from a device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPhotoAcquireSource</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/98859baa-a6bd-4b12-992b-af6736fa9650">GetDeviceIcons</a>
</td>
<td align="left" width="63%">
Retrieves the icons that are used to represent the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c997e76-9109-403f-821f-d73e8577b1ac">GetDeviceId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier (ID) of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406579">GetFriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device, formatted for display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c066464b-1d88-4d43-8bfd-0f60f21db5fd">GetItemAt</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem</a> object at the given index in the list of items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f60538f2-f1b1-40bb-8663-ed93eede433e">GetItemCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items found by the <a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">InitializeItemList</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4c01856-b7e4-4318-aaf8-8e34e441ce75">GetPhotoAcquireSettings</a>
</td>
<td align="left" width="63%">
Obtains an <a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings</a> object for working with acquisition settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">InitializeItemList</a>
</td>
<td align="left" width="63%">
Enumerates transferable items on the device and passes each item to the optional progress callback, if it is supplied.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

