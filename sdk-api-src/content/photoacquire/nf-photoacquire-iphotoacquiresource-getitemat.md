---
UID: NF:photoacquire.IPhotoAcquireSource.GetItemAt
title: IPhotoAcquireSource::GetItemAt (photoacquire.h)

description: The GetItemAt method retrieves the IPhotoAcquireItem object at the given index in the list of items.
old-location: picacq\iphotoacquiresource_getitemat.htm
tech.root: acquisition
ms.assetid: c066464b-1d88-4d43-8bfd-0f60f21db5fd

ms.date: 12/05/2018
ms.keywords: GetItemAt, GetItemAt method [Picture Acquisition], GetItemAt method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetItemAt method, IPhotoAcquireSource.GetItemAt, IPhotoAcquireSource::GetItemAt, IPhotoAcquireSourceGetItemAt, photoacquire/IPhotoAcquireSource::GetItemAt, picacq.iphotoacquiresource_getitemat
ms.topic: method
f1_keywords: 
 - "photoacquire/IPhotoAcquireSource.GetItemAt"
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
 - IPhotoAcquireSource.GetItemAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquireSource::GetItemAt


## -description



The <code>GetItemAt</code> method retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem</a> object at the given index in the list of items.




## -parameters




### -param nIndex [in]

Integer value containing the index.


### -param ppPhotoAcquireItem [out]

Pointer to the address of an <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem</a> object.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -remarks



Before calling this method, call <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-initializeitemlist">InitializeItemList</a> to initialize the item list.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource Interface</a>
 

 

