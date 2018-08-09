---
UID: NF:photoacquire.IPhotoAcquireOptionsDialog.Destroy
title: IPhotoAcquireOptionsDialog::Destroy
author: windows-sdk-content
description: The Destroy method closes and destroys the modeless dialog box created with the Create method.
old-location: picacq\iphotoacquireoptionsdialog_destroy.htm
old-project: acquisition
ms.assetid: 787e12e9-b134-416a-9191-5a2cc6a922fd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Destroy, Destroy method [Picture Acquisition], Destroy method [Picture Acquisition],IPhotoAcquireOptionsDialog interface, IPhotoAcquireOptionsDialog interface [Picture Acquisition],Destroy method, IPhotoAcquireOptionsDialog.Destroy, IPhotoAcquireOptionsDialog::Destroy, IPhotoAcquireOptionsDialogDestroy, photoacquire/IPhotoAcquireOptionsDialog::Destroy, picacq.iphotoacquireoptionsdialog_destroy
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
 - IPhotoAcquireOptionsDialog.Destroy
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPhotoAcquireOptionsDialog::Destroy


## -description



The <code>Destroy</code> method closes and destroys the modeless dialog box created with the <a href="https://msdn.microsoft.com/22eb58d2-f1cf-4115-a5d4-dceb1d3ba4ad">Create</a> method.




## -parameters






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



If you destroy the parent window, the child window will automatically be destroyed.




## -see-also




<a href="https://msdn.microsoft.com/075e188f-e533-403d-be06-6a3260479f1a">IPhotoAcquireOptionsDialog Interface</a>
 

 

