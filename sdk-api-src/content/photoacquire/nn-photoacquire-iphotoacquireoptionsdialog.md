---
UID: NN:photoacquire.IPhotoAcquireOptionsDialog
title: IPhotoAcquireOptionsDialog
author: windows-sdk-content
description: The IPhotoAcquireOptionsDialog interface is used to display an options dialog box in which the user can select photo acquisition settings such as file name formats, as well as whether or not to rotate images, to prompt for a tag name, or to erase photos from the camera after importing.
old-location: picacq\iphotoacquireoptionsdialog.htm
tech.root: acquisition
ms.assetid: 075e188f-e533-403d-be06-6a3260479f1a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPhotoAcquireOptionsDialog, IPhotoAcquireOptionsDialog interface [Picture Acquisition], IPhotoAcquireOptionsDialog interface [Picture Acquisition],described, IPhotoAcquireOptionsDialogInterface, photoacquire/IPhotoAcquireOptionsDialog, picacq.iphotoacquireoptionsdialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireOptionsDialog interface


## -description



The <code>IPhotoAcquireOptionsDialog</code> interface is used to display an options dialog box in which the user can select photo acquisition settings such as file name formats, as well as whether or not to rotate images, to prompt for a tag name, or to erase photos from the camera after importing.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireOptionsDialog</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPhotoAcquireOptionsDialog</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/22eb58d2-f1cf-4115-a5d4-dceb1d3ba4ad">Create</a>
</td>
<td align="left" width="63%">
Creates and displays a modeless instance of the photo options dialog box, hosted within a parent window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/787e12e9-b134-416a-9191-5a2cc6a922fd">Destroy</a>
</td>
<td align="left" width="63%">
Closes and destroys the modeless dialog box created with the <a href="https://msdn.microsoft.com/22eb58d2-f1cf-4115-a5d4-dceb1d3ba4ad">Create</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbceebc3-10dd-4028-9672-1976a459cafe">DoModal</a>
</td>
<td align="left" width="63%">
Creates and displays the options dialog box as a modal dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e3c7876-28a6-4d5f-afca-7c0421df8c02">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the options dialog box and reads any saved options from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/271c2bfb-67a9-4998-90d1-4ed61f89aa03">SaveData</a>
</td>
<td align="left" width="63%">
Saves the acquisition settings from the options dialog box to the registry, so that a subsequent instance of the dialog can be initialized with the same settings.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f58529da-f419-445a-879a-2c087b770f0f">Interfaces</a>
 

 

