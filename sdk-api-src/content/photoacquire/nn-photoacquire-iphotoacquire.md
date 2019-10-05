---
UID: NN:photoacquire.IPhotoAcquire
title: IPhotoAcquire (photoacquire.h)
author: windows-sdk-content
description: The IPhotoAcquire interface provides methods for acquiring photos from a device.
old-location: picacq\iphotoacquire.htm
tech.root: acquisition
ms.assetid: 94f41290-bbc4-4a2f-9787-831004bde3c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPhotoAcquire, IPhotoAcquire interface [Picture Acquisition], IPhotoAcquire interface [Picture Acquisition],described, IPhotoAcquireInterface, photoacquire/IPhotoAcquire, picacq.iphotoacquire
ms.topic: interface
f1_keywords: 
 - "photoacquire/IPhotoAcquire"
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
 - IPhotoAcquire
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquire interface


## -description



The <code>IPhotoAcquire</code> interface provides methods for acquiring photos from a device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquire</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhotoAcquire</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoAcquire</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">Acquire</a>
</td>
<td align="left" width="63%">
Acquires photos from a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-createphotosource">CreatePhotoSource</a>
</td>
<td align="left" width="63%">
Initializes the source from which to acquire photos.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-enumresults">EnumResults</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of the acquired files.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/interfaces">Interfaces</a>
 

 

