---
UID: NF:photoacquire.IPhotoAcquireDeviceSelectionDialog.SetTitle
title: IPhotoAcquireDeviceSelectionDialog::SetTitle (photoacquire.h)
author: windows-sdk-content
description: The SetTitle method sets the title of the device selection dialog box.
old-location: picacq\iphotoacquiredeviceselectiondialog_settitle.htm
tech.root: acquisition
ms.assetid: e8338978-3232-41b2-87ee-11eee3e90fc6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPhotoAcquireDeviceSelectionDialog interface [Picture Acquisition],SetTitle method, IPhotoAcquireDeviceSelectionDialog.SetTitle, IPhotoAcquireDeviceSelectionDialog::SetTitle, IPhotoAcquireDeviceSelectionDialogSetTitle, SetTitle, SetTitle method [Picture Acquisition], SetTitle method [Picture Acquisition],IPhotoAcquireDeviceSelectionDialog interface, photoacquire/IPhotoAcquireDeviceSelectionDialog::SetTitle, picacq.iphotoacquiredeviceselectiondialog_settitle
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
 - IPhotoAcquireDeviceSelectionDialog.SetTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireDeviceSelectionDialog::SetTitle


## -description



The <code>SetTitle</code> method sets the title of the device selection dialog box.




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




<a href="https://msdn.microsoft.com/7ec649d2-9fd7-4c07-ad64-f3bc4acfc40d">IPhotoAcquireDeviceSelectionDialog Interface</a>
 

 

