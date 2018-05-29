---
UID: NF:photoacquire.IPhotoProgressDialog.GetWindow
title: IPhotoProgressDialog::GetWindow
author: windows-sdk-content
description: The GetWindow method retrieves the handle to the progress dialog box.
old-location: picacq\iphotoprogressdialog_getwindow.htm
old-project: acquisition
ms.assetid: c407e0a6-676f-419d-ab9a-85f5d0dcc480
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: GetWindow, GetWindow method [Picture Acquisition], GetWindow method [Picture Acquisition],IPhotoProgressDialog interface, IPhotoProgressDialog interface [Picture Acquisition],GetWindow method, IPhotoProgressDialog.GetWindow, IPhotoProgressDialog::GetWindow, IPhotoProgressDialogGetWindow, photoacquire/IPhotoProgressDialog::GetWindow, picacq.iphotoprogressdialog_getwindow
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
-	IPhotoProgressDialog.GetWindow
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/a3928874-5a15-43d9-9d9c-8b66478b0597">IPhotoProgressDialog Interface</a>
 

 

