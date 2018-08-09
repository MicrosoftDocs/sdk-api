---
UID: NF:photoacquire.IPhotoAcquireProgressCB.EndDelete
title: IPhotoAcquireProgressCB::EndDelete
author: windows-sdk-content
description: The EndDelete method provides extended functionality when deletion of files from the image source is complete. The application provides the implementation of the EndDelete method.
old-location: picacq\iphotoacquireprogresscb_enddelete.htm
old-project: acquisition
ms.assetid: bc5879a9-851b-4b22-99bb-814464c2712d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EndDelete, EndDelete method [Picture Acquisition], EndDelete method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],EndDelete method, IPhotoAcquireProgressCB.EndDelete, IPhotoAcquireProgressCB::EndDelete, IPhotoAcquireProgressCBEndDelete, photoacquire/IPhotoAcquireProgressCB::EndDelete, picacq.iphotoacquireprogresscb_enddelete
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireProgressCB.EndDelete
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPhotoAcquireProgressCB::EndDelete


## -description



The <code>EndDelete</code> method provides extended functionality when deletion of files from the image source is complete. The application provides the implementation of the <code>EndDelete</code> method.




## -parameters




### -param hr [in]

Specifies the result of the delete operation.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not yet implemented

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>
 

 

