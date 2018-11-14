---
UID: NF:photoacquire.IPhotoProgressDialog.SetCheckboxTooltip
title: IPhotoProgressDialog::SetCheckboxTooltip
author: windows-sdk-content
description: The SetCheckboxTooltip method sets the tooltip text for the check box in the progress dialog box.
old-location: picacq\iphotoprogressdialog_setcheckboxtooltip.htm
tech.root: acquisition
ms.assetid: 88719891-9661-4766-adce-6b74cf9a87ef
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],SetCheckboxTooltip method, IPhotoProgressDialog.SetCheckboxTooltip, IPhotoProgressDialog::SetCheckboxTooltip, IPhotoProgressDialogSetCheckboxTooltip, SetCheckboxTooltip, SetCheckboxTooltip method [Picture Acquisition], SetCheckboxTooltip method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::SetCheckboxTooltip, picacq.iphotoprogressdialog_setcheckboxtooltip
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
 - IPhotoProgressDialog.SetCheckboxTooltip
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
- IPhotoProgressDialog.SetCheckboxTooltip
: 
---

# IPhotoProgressDialog::SetCheckboxTooltip


## -description



The <code>SetCheckboxTooltip</code> method sets the tooltip text for the check box in the progress dialog box.




## -parameters




### -param nCheckboxId [in]

Integer containing the check box identifier (ID).


### -param pszCheckboxTooltipText [in]

Pointer to a null-terminated string containing the check box tooltip text.


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
 

 

