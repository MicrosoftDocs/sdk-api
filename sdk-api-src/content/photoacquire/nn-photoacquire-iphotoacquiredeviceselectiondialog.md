---
UID: NN:photoacquire.IPhotoAcquireDeviceSelectionDialog
title: IPhotoAcquireDeviceSelectionDialog (photoacquire.h)
description: Provides a dialog box for selecting the device to acquire images from.helpviewer_keywords: ["IPhotoAcquireDeviceSelectionDialog","IPhotoAcquireDeviceSelectionDialog interface [Picture Acquisition]","IPhotoAcquireDeviceSelectionDialog interface [Picture Acquisition]","described","IPhotoAcquireDeviceSelectionDialogInterface","photoacquire/IPhotoAcquireDeviceSelectionDialog","picacq.iphotoacquiredeviceselectiondialog"]
old-location: picacq\iphotoacquiredeviceselectiondialog.htm
tech.root: acquisition
ms.assetid: 7ec649d2-9fd7-4c07-ad64-f3bc4acfc40d
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireDeviceSelectionDialog, IPhotoAcquireDeviceSelectionDialog interface [Picture Acquisition], IPhotoAcquireDeviceSelectionDialog interface [Picture Acquisition],described, IPhotoAcquireDeviceSelectionDialogInterface, photoacquire/IPhotoAcquireDeviceSelectionDialog, picacq.iphotoacquiredeviceselectiondialog
f1_keywords:
- photoacquire/IPhotoAcquireDeviceSelectionDialog
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- photoacquire.h
api_name:
- IPhotoAcquireDeviceSelectionDialog
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquireDeviceSelectionDialog interface


## -description



Provides a dialog box for selecting the device to acquire images from.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireDeviceSelectionDialog</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhotoAcquireDeviceSelectionDialog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoAcquireDeviceSelectionDialog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiredeviceselectiondialog-domodal">DoModal</a>
</td>
<td align="left" width="63%">
Displays a device selection dialog box and retrieves the ID and type of the selected device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiredeviceselectiondialog-setsubmitbuttontext">SetPrompt</a>
</td>
<td align="left" width="63%">
Sets the text displayed in the dialog box that prompts the user to select a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiredeviceselectiondialog-settitle">SetTitle</a>
</td>
<td align="left" width="63%">
Sets the title of the device selection dialog box.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/interfaces">Interfaces</a>
 

 

