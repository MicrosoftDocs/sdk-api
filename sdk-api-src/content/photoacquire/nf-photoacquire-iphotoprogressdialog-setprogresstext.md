---
UID: NF:photoacquire.IPhotoProgressDialog.SetProgressText
title: IPhotoProgressDialog::SetProgressText
author: windows-sdk-content
description: The SetProgressText method sets the text for the progress bar in the progress dialog box.
old-location: picacq\iphotoprogressdialog_setprogresstext.htm
old-project: acquisition
ms.assetid: b3210667-1fe2-4b30-9e5e-311f720647ce
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],SetProgressText method, IPhotoProgressDialog.SetProgressText, IPhotoProgressDialog::SetProgressText, IPhotoProgressDialogSetProgressText, SetProgressText, SetProgressText method [Picture Acquisition], SetProgressText method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::SetProgressText, picacq.iphotoprogressdialog_setprogresstext
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
 - IPhotoProgressDialog.SetProgressText
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPhotoProgressDialog::SetProgressText


## -description



The <code>SetProgressText</code> method sets the text for the progress bar in the progress dialog box.




## -parameters




### -param pszProgressText [in]

Pointer to a null-terminated string containing the progress text.


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
 

 

