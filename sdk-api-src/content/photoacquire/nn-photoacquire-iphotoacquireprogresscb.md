---
UID: NN:photoacquire.IPhotoAcquireProgressCB
title: IPhotoAcquireProgressCB
author: windows-driver-content
description: The IPhotoAcquireProgressCB interface may be implemented if you wish to do extra processing at various stages in the acquisition process.
old-location: picacq\iphotoacquireprogresscb.htm
old-project: acquisition
ms.assetid: c4fcc470-1b05-4d33-8581-80c6e7488e04
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPhotoAcquireProgressCB, IPhotoAcquireProgressCB interface [Picture Acquisition], IPhotoAcquireProgressCB interface [Picture Acquisition], described, IPhotoAcquireProgressCBInterface, photoacquire/IPhotoAcquireProgressCB, picacq.iphotoacquireprogresscb
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	photoacquire.h
api_name:
-	IPhotoAcquireProgressCB
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPhotoAcquireProgressCB interface


## -description



The <code>IPhotoAcquireProgressCB</code> interface may be implemented if you wish to do extra processing at various stages in the acquisition process.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireProgressCB</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPhotoAcquireProgressCB</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7a37934c-dc0b-433e-99cf-6c26341e582c">Cancelled</a>
</td>
<td align="left" width="63%">
Provides extended functionality when a cancellation occurs during an acquisition session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c784750c-3f73-4ebb-ad38-cc05aada0fca">DirectoryCreated</a>
</td>
<td align="left" width="63%">
Provides extended functionality when a destination directory is created during the acquisition process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc5879a9-851b-4b22-99bb-814464c2712d">EndDelete</a>
</td>
<td align="left" width="63%">
Provides extended functionality when deletion of files from the image source is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dac16ca2-bd80-4771-9e81-09d07958a4bb">EndEnumeration</a>
</td>
<td align="left" width="63%">
Provides extended functionality when enumeration of files from the image source is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2962b170-941f-4cf1-9969-4066ee0c57d9">EndItemDelete</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time a file is deleted from the image source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d2c0773-cb0b-4cc3-b61f-9ad4153bcf96">EndItemTransfer</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time a file is transferred from the image source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543004">EndSession</a>
</td>
<td align="left" width="63%">
Provides extended functionality when an acquisition session is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e0fada0-6c83-4e82-a3ac-c5a4832f053f">EndTransfer</a>
</td>
<td align="left" width="63%">
Provides extended functionality when transfer of all files from an image source is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">ErrorAdvise</a>
</td>
<td align="left" width="63%">
Provides custom error handling for errors that occur during acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b80fb2f2-57b7-4333-891e-32eba0347a17">FoundItem</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time an item is found during enumeration of items from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9e3fb54-e152-4fbd-b745-852719aabeec">GetDeleteAfterAcquire</a>
</td>
<td align="left" width="63%">
Returns a value indicating whether files should be deleted after download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db0d924b-a586-4f81-a367-e8fbdf3e9bd9">GetUserInput</a>
</td>
<td align="left" width="63%">
Overrides the default functionality that displays a message prompting the user for string input during acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/510999eb-068e-41e9-98b7-de6e67dbfe2f">StartDelete</a>
</td>
<td align="left" width="63%">
Provides extended functionality when deletion of items from the device begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef42722d-ca39-4d22-8de1-6b3926669abf">StartEnumeration</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the enumeration of items to acquire begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f4ab29d-ea9c-410d-94ab-4c4d8ed76b4d">StartItemDelete</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time the deletion of an individual item from the device begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fffd9313-fbed-493b-a82e-1ccd202859c0">StartItemTransfer</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time the transfer of an item begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fff67d0-5d0a-4d8d-bc59-55cb65b77147">StartTransfer</a>
</td>
<td align="left" width="63%">
Provides extended functionality when acquisition of images from the device begins

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b555d9b-1d01-43ad-b267-8d53023390e8">UpdateDeletePercent</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the percentage of items deleted changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a868663d-f926-4b29-9e1f-7df4ec36687b">UpdateTransferPercent</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the percentage of items transferred changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

