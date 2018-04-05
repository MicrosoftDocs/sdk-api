---
UID: NF:photoacquire.IPhotoProgressDialog.SetPercentComplete
title: IPhotoProgressDialog::SetPercentComplete method
author: windows-driver-content
description: The SetPercentComplete method sets a value indicating the completed portion of the current operation.
old-location: picacq\iphotoprogressdialog_setpercentcomplete.htm
old-project: acquisition
ms.assetid: b2fb225d-6d2b-49f7-bbc9-715107e90df2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPhotoProgressDialog, IPhotoProgressDialog interface [Picture Acquisition], SetPercentComplete method, IPhotoProgressDialog::SetPercentComplete, IPhotoProgressDialogSetPercentComplete, SetPercentComplete method [Picture Acquisition], SetPercentComplete method [Picture Acquisition], IPhotoProgressDialog interface, SetPercentComplete,IPhotoProgressDialog.SetPercentComplete, photoacquire/IPhotoProgressDialog::SetPercentComplete, picacq.iphotoprogressdialog_setpercentcomplete
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PhotoAcquireUID.lib
-	PhotoAcquireUID.dll
api_name:
-	IPhotoProgressDialog.SetPercentComplete
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPhotoProgressDialog::SetPercentComplete method


## -description



The <code>SetPercentComplete</code> method sets a value indicating the completed portion of the current operation.




## -parameters




### -param nPercent [in]

Integer value indicating the percentage of the operation that has completed. This value may be between 0 and 100 only.


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



If you pass PROGRESS_INDETERMINATE to <code>SetPercentComplete</code>, the progress bar will not progress from left to right (from 0 to 100%), but will instead animate to indicate that an operation with an indeterminate end is taking place.




## -see-also




<a href="https://msdn.microsoft.com/a3928874-5a15-43d9-9d9c-8b66478b0597">IPhotoProgressDialog Interface</a>
 

 

