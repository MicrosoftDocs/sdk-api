---
UID: NF:photoacquire.IPhotoProgressDialog.SetTitle
title: IPhotoProgressDialog::SetTitle
author: windows-sdk-content
description: The SetTitle method sets the title of the progress dialog box.
old-location: picacq\iphotoprogressdialog_settitle.htm
tech.root: acquisition
ms.assetid: ee1f8b8e-bc46-4699-a682-2933c18a794b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],SetTitle method, IPhotoProgressDialog.SetTitle, IPhotoProgressDialog::SetTitle, IPhotoProgressDialogSetTitle, SetTitle, SetTitle method [Picture Acquisition], SetTitle method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::SetTitle, picacq.iphotoprogressdialog_settitle
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
 - IPhotoProgressDialog.SetTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoProgressDialog::SetTitle


## -description



The <code>SetTitle</code> method sets the title of the progress dialog box.




## -parameters




### -param pszTitle [in]

Pointer to a null-terminated string containing the title.


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
 

 

