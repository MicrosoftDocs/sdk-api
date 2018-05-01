---
UID: NF:photoacquire.IPhotoAcquireDeviceSelectionDialog.SetTitle
title: IPhotoAcquireDeviceSelectionDialog::SetTitle method
author: windows-driver-content
description: The SetTitle method sets the title of the device selection dialog box.
old-location: picacq\iphotoacquiredeviceselectiondialog_settitle.htm
old-project: acquisition
ms.assetid: e8338978-3232-41b2-87ee-11eee3e90fc6
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPhotoAcquireDeviceSelectionDialog, IPhotoAcquireDeviceSelectionDialog interface [Picture Acquisition], SetTitle method, IPhotoAcquireDeviceSelectionDialog::SetTitle, IPhotoAcquireDeviceSelectionDialogSetTitle, SetTitle method [Picture Acquisition], SetTitle method [Picture Acquisition], IPhotoAcquireDeviceSelectionDialog interface, SetTitle,IPhotoAcquireDeviceSelectionDialog.SetTitle, photoacquire/IPhotoAcquireDeviceSelectionDialog::SetTitle, picacq.iphotoacquiredeviceselectiondialog_settitle
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
-	IPhotoAcquireDeviceSelectionDialog.SetTitle
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPhotoAcquireDeviceSelectionDialog::SetTitle method


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
 

 

