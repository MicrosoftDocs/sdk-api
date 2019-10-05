---
UID: NN:photoacquire.IPhotoAcquireProgressCB
title: IPhotoAcquireProgressCB (photoacquire.h)
author: windows-sdk-content
description: The IPhotoAcquireProgressCB interface may be implemented if you wish to do extra processing at various stages in the acquisition process.
old-location: picacq\iphotoacquireprogresscb.htm
tech.root: acquisition
ms.assetid: c4fcc470-1b05-4d33-8581-80c6e7488e04
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireProgressCB, IPhotoAcquireProgressCB interface [Picture Acquisition], IPhotoAcquireProgressCB interface [Picture Acquisition],described, IPhotoAcquireProgressCBInterface, photoacquire/IPhotoAcquireProgressCB, picacq.iphotoacquireprogresscb
ms.topic: interface
f1_keywords: 
 - "photoacquire/IPhotoAcquireProgressCB"
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
 - IPhotoAcquireProgressCB
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquireProgressCB interface


## -description



The <code>IPhotoAcquireProgressCB</code> interface may be implemented if you wish to do extra processing at various stages in the acquisition process.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireProgressCB</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhotoAcquireProgressCB</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoAcquireProgressCB</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-cancelled">Cancelled</a>
</td>
<td align="left" width="63%">
Provides extended functionality when a cancellation occurs during an acquisition session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-directorycreated">DirectoryCreated</a>
</td>
<td align="left" width="63%">
Provides extended functionality when a destination directory is created during the acquisition process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-enddelete">EndDelete</a>
</td>
<td align="left" width="63%">
Provides extended functionality when deletion of files from the image source is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-endenumeration">EndEnumeration</a>
</td>
<td align="left" width="63%">
Provides extended functionality when enumeration of files from the image source is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-enditemdelete">EndItemDelete</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time a file is deleted from the image source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-enditemtransfer">EndItemTransfer</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time a file is transferred from the image source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-endsession">EndSession</a>
</td>
<td align="left" width="63%">
Provides extended functionality when an acquisition session is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-endtransfer">EndTransfer</a>
</td>
<td align="left" width="63%">
Provides extended functionality when transfer of all files from an image source is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">ErrorAdvise</a>
</td>
<td align="left" width="63%">
Provides custom error handling for errors that occur during acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-founditem">FoundItem</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time an item is found during enumeration of items from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-getdeleteafteracquire">GetDeleteAfterAcquire</a>
</td>
<td align="left" width="63%">
Returns a value indicating whether files should be deleted after download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-getuserinput">GetUserInput</a>
</td>
<td align="left" width="63%">
Overrides the default functionality that displays a message prompting the user for string input during acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-startdelete">StartDelete</a>
</td>
<td align="left" width="63%">
Provides extended functionality when deletion of items from the device begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-startenumeration">StartEnumeration</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the enumeration of items to acquire begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-startitemdelete">StartItemDelete</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time the deletion of an individual item from the device begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-startitemtransfer">StartItemTransfer</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time the transfer of an item begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-starttransfer">StartTransfer</a>
</td>
<td align="left" width="63%">
Provides extended functionality when acquisition of images from the device begins

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-updatedeletepercent">UpdateDeletePercent</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the percentage of items deleted changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-updatetransferpercent">UpdateTransferPercent</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the percentage of items transferred changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/interfaces">Interfaces</a>
 

 

