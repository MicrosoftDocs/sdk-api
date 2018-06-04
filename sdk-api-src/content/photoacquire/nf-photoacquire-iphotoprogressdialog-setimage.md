---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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




<a href="https://msdn.microsoft.com/a3928874-5a15-43d9-9d9c-8b66478b0597">IPhotoProgressDialog Interface</a>
 

 

