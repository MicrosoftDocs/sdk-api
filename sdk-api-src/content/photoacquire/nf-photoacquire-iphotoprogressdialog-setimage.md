---
UID: NF:photoacquire.IPhotoProgressDialog.SetImage
title: IPhotoProgressDialog::SetImage (photoacquire.h)
description: Sets either the thumbnail image displayed in the progress dialog box, the icon in the title bar of the progress dialog box, or the icon in ALT+TAB key combination windows.
helpviewer_keywords: ["IPhotoProgressDialog interface [Picture Acquisition]","SetImage method","IPhotoProgressDialog.SetImage","IPhotoProgressDialog::SetImage","IPhotoProgressDialogSetImage","PROGRESS_DIALOG_BITMAP_THUMBNAIL","PROGRESS_DIALOG_ICON_LARGE","PROGRESS_DIALOG_ICON_SMALL","PROGRESS_DIALOG_ICON_THUMBNAIL","SetImage","SetImage method [Picture Acquisition]","SetImage method [Picture Acquisition]","IPhotoProgressDialog interface","photoacquire/IPhotoProgressDialog::SetImage","picacq.iphotoprogressdialog_setimage"]
old-location: picacq\iphotoprogressdialog_setimage.htm
tech.root: picacq
ms.assetid: 45b795c4-4f95-4132-86a7-cda47e534e9c
ms.date: 12/05/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],SetImage method, IPhotoProgressDialog.SetImage, IPhotoProgressDialog::SetImage, IPhotoProgressDialogSetImage, PROGRESS_DIALOG_BITMAP_THUMBNAIL, PROGRESS_DIALOG_ICON_LARGE, PROGRESS_DIALOG_ICON_SMALL, PROGRESS_DIALOG_ICON_THUMBNAIL, SetImage, SetImage method [Picture Acquisition], SetImage method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::SetImage, picacq.iphotoprogressdialog_setimage
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
 - IPhotoProgressDialog::SetImage
 - photoacquire/IPhotoProgressDialog::SetImage
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
 - IPhotoProgressDialog.SetImage
---

# IPhotoProgressDialog::SetImage


## -description

Sets either the thumbnail image displayed in the progress dialog box, the icon in the title bar of the progress dialog box, or the icon in ALT+TAB key combination windows.

## -parameters

### -param nImageType [in]

Integer value indicating the image type to set. Only one type of image type may be set at a time. The values passed to this parameter should not be considered a bit field and may not be combined with bitwise OR. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROGRESS_DIALOG_ICON_SMALL"></a><a id="progress_dialog_icon_small"></a><dl>
<dt><b>PROGRESS_DIALOG_ICON_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The small icon used in the title bar (normally 16 x 16 pixels).

</td>
</tr>
<tr>
<td width="40%"><a id="PROGRESS_DIALOG_ICON_LARGE"></a><a id="progress_dialog_icon_large"></a><dl>
<dt><b>PROGRESS_DIALOG_ICON_LARGE</b></dt>
</dl>
</td>
<td width="60%">
The icon used to represent the progress dialog box in Alt-Tab windows (normally 32 x 32 pixels).

</td>
</tr>
<tr>
<td width="40%"><a id="PROGRESS_DIALOG_ICON_THUMBNAIL"></a><a id="progress_dialog_icon_thumbnail"></a><dl>
<dt><b>PROGRESS_DIALOG_ICON_THUMBNAIL</b></dt>
</dl>
</td>
<td width="60%">
An icon used in place of the thumbnail (up to 128 x 128 pixels).

</td>
</tr>
<tr>
<td width="40%"><a id="PROGRESS_DIALOG_BITMAP_THUMBNAIL"></a><a id="progress_dialog_bitmap_thumbnail"></a><dl>
<dt><b>PROGRESS_DIALOG_BITMAP_THUMBNAIL</b></dt>
</dl>
</td>
<td width="60%">
A bitmap thumbnail (up to 128 x 128 pixels, although it will be scaled to fit if it is too large).

</td>
</tr>
</table>

### -param hIcon [in]

Handle to an icon object.

### -param hBitmap [in]

Handle to a bitmap object representing the thumbnail image.

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

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoprogressdialog">IPhotoProgressDialog Interface</a>