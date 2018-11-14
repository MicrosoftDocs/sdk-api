---
UID: NF:photoacquire.IPhotoAcquireOptionsDialog.Create
title: IPhotoAcquireOptionsDialog::Create
author: windows-sdk-content
description: The Create method creates and displays a modeless instance of the photo options dialog box, hosted within a parent window.
old-location: picacq\iphotoacquireoptionsdialog_create.htm
tech.root: acquisition
ms.assetid: 22eb58d2-f1cf-4115-a5d4-dceb1d3ba4ad
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Create, Create method [Picture Acquisition], Create method [Picture Acquisition],IPhotoAcquireOptionsDialog interface, IPhotoAcquireOptionsDialog interface [Picture Acquisition],Create method, IPhotoAcquireOptionsDialog.Create, IPhotoAcquireOptionsDialog::Create, IPhotoAcquireOptionsDialogCreate, photoacquire/IPhotoAcquireOptionsDialog::Create, picacq.iphotoacquireoptionsdialog_create
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
 - IPhotoAcquireOptionsDialog.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- photoacquire.h
: 
- IPhotoAcquireOptionsDialog.Create
: 
---

# IPhotoAcquireOptionsDialog::Create


## -description



The <code>Create</code> method creates and displays a modeless instance of the photo options dialog box, hosted within a parent window.




## -parameters




### -param hWndParent [in]

Handle to the parent window.


### -param phWndDialog [out]

Specifies the created dialog box.


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



The <a href="https://msdn.microsoft.com/6e3c7876-28a6-4d5f-afca-7c0421df8c02">Initialize</a> method should be called prior to the <code>Create</code> method.

The parent window indicated by <i>hWndParent</i> provides <b>OK</b> and <b>Cancel</b> buttons to the new dialog box instance.




## -see-also




<a href="https://msdn.microsoft.com/075e188f-e533-403d-be06-6a3260479f1a">IPhotoAcquireOptionsDialog Interface</a>
 

 

