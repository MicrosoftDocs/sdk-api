---
UID: NF:photoacquire.IPhotoProgressDialog.SetCheckboxText
title: IPhotoProgressDialog::SetCheckboxText
author: windows-sdk-content
description: The SetCheckboxText method sets the text for the check box in the progress dialog box indicating whether to delete images after transfer.
old-location: picacq\iphotoprogressdialog_setcheckboxtext.htm
tech.root: acquisition
ms.assetid: db516dcd-90b4-4421-b883-2f8462b36249
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],SetCheckboxText method, IPhotoProgressDialog.SetCheckboxText, IPhotoProgressDialog::SetCheckboxText, IPhotoProgressDialogSetCheckboxText, SetCheckboxText, SetCheckboxText method [Picture Acquisition], SetCheckboxText method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::SetCheckboxText, picacq.iphotoprogressdialog_setcheckboxtext
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
 - IPhotoProgressDialog.SetCheckboxText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoProgressDialog::SetCheckboxText


## -description



The <code>SetCheckboxText</code> method sets the text for the check box in the progress dialog box indicating whether to delete images after transfer.




## -parameters




### -param nCheckboxId [in]

Integer containing the check box identifier (ID).


### -param pszCheckboxText [in]

Pointer to a null-terminated string containing the check box text.


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
 

 

