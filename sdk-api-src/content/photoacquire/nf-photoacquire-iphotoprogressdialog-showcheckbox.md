---
UID: NF:photoacquire.IPhotoProgressDialog.ShowCheckbox
title: IPhotoProgressDialog::ShowCheckbox
author: windows-sdk-content
description: The ShowCheckbox method indicates whether to show the check box in the progress dialog box indicating whether to delete images after transfer.
old-location: picacq\iphotoprogressdialog_showcheckbox.htm
old-project: acquisition
ms.assetid: 6518c073-b4d9-49df-819f-473028ad230a
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],ShowCheckbox method, IPhotoProgressDialog.ShowCheckbox, IPhotoProgressDialog::ShowCheckbox, IPhotoProgressDialogShowCheckbox, ShowCheckbox, ShowCheckbox method [Picture Acquisition], ShowCheckbox method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::ShowCheckbox, picacq.iphotoprogressdialog_showcheckbox
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PhotoAcquireUID.lib
-	PhotoAcquireUID.dll
api_name:
-	IPhotoProgressDialog.ShowCheckbox
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPhotoProgressDialog::ShowCheckbox


## -description



The <code>ShowCheckbox</code> method indicates whether to show the check box in the progress dialog box indicating whether to delete images after transfer.




## -parameters




### -param nCheckboxId [in]

Integer containing the check box identifier (ID).


### -param fShow [in]

Flag that, when set to <b>TRUE</b>, indicates that the check box will appear.


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
 




## -see-also




<a href="https://msdn.microsoft.com/a3928874-5a15-43d9-9d9c-8b66478b0597">IPhotoProgressDialog Interface</a>
 

 

