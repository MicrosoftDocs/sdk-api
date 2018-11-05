---
UID: NF:photoacquire.IPhotoAcquireProgressCB.FoundItem
title: IPhotoAcquireProgressCB::FoundItem
author: windows-sdk-content
description: The FoundItem method provides extended functionality each time an item is found during enumeration of items from the device.
old-location: picacq\iphotoacquireprogresscb_founditem.htm
tech.root: acquisition
ms.assetid: b80fb2f2-57b7-4333-891e-32eba0347a17
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FoundItem, FoundItem method [Picture Acquisition], FoundItem method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB, IPhotoAcquireProgressCB interface [Picture Acquisition],FoundItem method, IPhotoAcquireProgressCB.FoundItem, IPhotoAcquireProgressCB::FoundItem, photoacquire/IPhotoAcquireProgressCB::FoundItem, picacq.iphotoacquireprogresscb_founditem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireProgressCB.FoundItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireProgressCB::FoundItem


## -description



The <code>FoundItem</code> method provides extended functionality each time an item is found during enumeration of items from the device. This method can be used to exclude an item from the list of items to acquire. The application provides the implementation of the <code>FoundItem</code> method.




## -parameters




### -param pPhotoAcquireItem [in]

Pointer to the found <a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem</a> object.


## -returns



The method returns an <b>HRESULT</b>. Your implementation is not limited to the following return values. Any failing HRESULT other than E_NOTIMPL is fatal and will cause the transfer to abort.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Exclude this item from the list of files to acquire.

</td>
</tr>
</table>
 




## -remarks



Return S_FALSE to exclude the item from the results of the enumeration. This would allow the caller to exclude videos or camera raw files, for instance.




## -see-also




<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>
 

 

