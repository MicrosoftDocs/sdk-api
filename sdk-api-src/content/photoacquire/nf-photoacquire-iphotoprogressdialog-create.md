---
UID: NF:photoacquire.IPhotoProgressDialog.Create
title: IPhotoProgressDialog::Create
author: windows-sdk-content
description: The Create method creates and displays a progress dialog box that can be shown during image enumeration and acquisition.
old-location: picacq\iphotoprogressdialog_create.htm
tech.root: acquisition
ms.assetid: e68ac203-f97b-4459-b344-c845f0ac0f1b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Create, Create method [Picture Acquisition], Create method [Picture Acquisition],IPhotoProgressDialog interface, IPhotoProgressDialog interface [Picture Acquisition],Create method, IPhotoProgressDialog.Create, IPhotoProgressDialog::Create, IPhotoProgressDialogCreate, photoacquire/IPhotoProgressDialog::Create, picacq.iphotoprogressdialog_create
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
 - IPhotoProgressDialog.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoProgressDialog::Create


## -description



The <code>Create</code> method creates and displays a progress dialog box that can be shown during image enumeration and acquisition.




## -parameters




### -param hwndParent [in]

Handle of the parent window.


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



The dialog box that is created is modal, and runs in its own thread.

To close the dialog, call <a href="https://msdn.microsoft.com/8690c67b-5f96-4e8c-8685-91fe5ed65511">Destroy</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3928874-5a15-43d9-9d9c-8b66478b0597">IPhotoProgressDialog Interface</a>



<a href="https://msdn.microsoft.com/8690c67b-5f96-4e8c-8685-91fe5ed65511">IPhotoProgressDialog::Destroy</a>
 

 

