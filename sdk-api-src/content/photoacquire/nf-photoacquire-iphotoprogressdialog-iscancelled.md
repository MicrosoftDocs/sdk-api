---
UID: NF:photoacquire.IPhotoProgressDialog.IsCancelled
title: IPhotoProgressDialog::IsCancelled (photoacquire.h)
author: windows-sdk-content
description: The IsCancelled method indicates whether the operation has been canceled via the progress dialog box.
old-location: picacq\iphotoprogressdialog_iscancelled.htm
tech.root: acquisition
ms.assetid: 0bd84b1f-7a2a-40eb-ba77-21a8f701e5e0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],IsCancelled method, IPhotoProgressDialog.IsCancelled, IPhotoProgressDialog::IsCancelled, IPhotoProgressDialogIsCancelled, IsCancelled, IsCancelled method [Picture Acquisition], IsCancelled method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::IsCancelled, picacq.iphotoprogressdialog_iscancelled
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
 - IPhotoProgressDialog.IsCancelled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoProgressDialog::IsCancelled


## -description



The <code>IsCancelled</code> method indicates whether the operation has been canceled via the progress dialog box.




## -parameters




### -param pfCancelled [out]

Pointer to a flag that, if set to <b>TRUE</b>, indicates the action has been canceled.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was passed

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a3928874-5a15-43d9-9d9c-8b66478b0597">IPhotoProgressDialog Interface</a>
 

 

