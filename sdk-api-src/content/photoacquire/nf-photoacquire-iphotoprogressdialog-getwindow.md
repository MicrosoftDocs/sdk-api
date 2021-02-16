---
UID: NF:photoacquire.IPhotoProgressDialog.GetWindow
title: IPhotoProgressDialog::GetWindow (photoacquire.h)
description: The GetWindow method retrieves the handle to the progress dialog box.
helpviewer_keywords: ["GetWindow","GetWindow method [Picture Acquisition]","GetWindow method [Picture Acquisition]","IPhotoProgressDialog interface","IPhotoProgressDialog interface [Picture Acquisition]","GetWindow method","IPhotoProgressDialog.GetWindow","IPhotoProgressDialog::GetWindow","IPhotoProgressDialogGetWindow","photoacquire/IPhotoProgressDialog::GetWindow","picacq.iphotoprogressdialog_getwindow"]
old-location: picacq\iphotoprogressdialog_getwindow.htm
tech.root: picacq
ms.assetid: c407e0a6-676f-419d-ab9a-85f5d0dcc480
ms.date: 12/05/2018
ms.keywords: GetWindow, GetWindow method [Picture Acquisition], GetWindow method [Picture Acquisition],IPhotoProgressDialog interface, IPhotoProgressDialog interface [Picture Acquisition],GetWindow method, IPhotoProgressDialog.GetWindow, IPhotoProgressDialog::GetWindow, IPhotoProgressDialogGetWindow, photoacquire/IPhotoProgressDialog::GetWindow, picacq.iphotoprogressdialog_getwindow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPhotoProgressDialog::GetWindow
 - photoacquire/IPhotoProgressDialog::GetWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoProgressDialog.GetWindow
---

# IPhotoProgressDialog::GetWindow


## -description

The <code>GetWindow</code> method retrieves the handle to the progress dialog box.

## -parameters

### -param phwndProgressDialog [out]

Specifies the handle to the progress dialog box.

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
Pointer passed was <b>NULL</b>

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoprogressdialog">IPhotoProgressDialog Interface</a>