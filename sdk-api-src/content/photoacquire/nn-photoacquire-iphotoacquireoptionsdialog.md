---
UID: NN:photoacquire.IPhotoAcquireOptionsDialog
title: IPhotoAcquireOptionsDialog (photoacquire.h)
description: The IPhotoAcquireOptionsDialog interface is used to display an options dialog box in which the user can select photo acquisition settings such as file name formats, as well as whether or not to rotate images, to prompt for a tag name, or to erase photos from the camera after importing.helpviewer_keywords: ["IPhotoAcquireOptionsDialog","IPhotoAcquireOptionsDialog interface [Picture Acquisition]","IPhotoAcquireOptionsDialog interface [Picture Acquisition]","described","IPhotoAcquireOptionsDialogInterface","photoacquire/IPhotoAcquireOptionsDialog","picacq.iphotoacquireoptionsdialog"]
old-location: picacq\iphotoacquireoptionsdialog.htm
tech.root: acquisition
ms.assetid: 075e188f-e533-403d-be06-6a3260479f1a
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireOptionsDialog, IPhotoAcquireOptionsDialog interface [Picture Acquisition], IPhotoAcquireOptionsDialog interface [Picture Acquisition],described, IPhotoAcquireOptionsDialogInterface, photoacquire/IPhotoAcquireOptionsDialog, picacq.iphotoacquireoptionsdialog
f1_keywords:
- photoacquire/IPhotoAcquireOptionsDialog
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
- IPhotoAcquireOptionsDialog
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquireOptionsDialog interface


## -description



The <code>IPhotoAcquireOptionsDialog</code> interface is used to display an options dialog box in which the user can select photo acquisition settings such as file name formats, as well as whether or not to rotate images, to prompt for a tag name, or to erase photos from the camera after importing.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireOptionsDialog</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhotoAcquireOptionsDialog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoAcquireOptionsDialog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-create">Create</a>
</td>
<td align="left" width="63%">
Creates and displays a modeless instance of the photo options dialog box, hosted within a parent window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-destroy">Destroy</a>
</td>
<td align="left" width="63%">
Closes and destroys the modeless dialog box created with the <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-create">Create</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-domodal">DoModal</a>
</td>
<td align="left" width="63%">
Creates and displays the options dialog box as a modal dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the options dialog box and reads any saved options from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-savedata">SaveData</a>
</td>
<td align="left" width="63%">
Saves the acquisition settings from the options dialog box to the registry, so that a subsequent instance of the dialog can be initialized with the same settings.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/interfaces">Interfaces</a>
 

 

