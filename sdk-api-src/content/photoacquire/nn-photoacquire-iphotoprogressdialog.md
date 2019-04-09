---
UID: NN:photoacquire.IPhotoProgressDialog
title: IPhotoProgressDialog (photoacquire.h)
author: windows-sdk-content
description: Provides the progress dialog box that may be displayed when enumerating or importing images. The dialog box is modal and runs in its own thread.
old-location: picacq\iphotoprogressdialog.htm
tech.root: acquisition
ms.assetid: a3928874-5a15-43d9-9d9c-8b66478b0597
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPhotoProgressDialog, IPhotoProgressDialog interface [Picture Acquisition], IPhotoProgressDialog interface [Picture Acquisition],described, IPhotoProgressDialogInterface, photoacquire/IPhotoProgressDialog, picacq.iphotoprogressdialog
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
 - IPhotoProgressDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoProgressDialog interface


## -description



Provides the progress dialog box that may be displayed when enumerating or importing images. The dialog box is modal and runs in its own thread.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoProgressDialog</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPhotoProgressDialog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoProgressDialog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e68ac203-f97b-4459-b344-c845f0ac0f1b">Create</a>
</td>
<td align="left" width="63%">
Creates and displays a progress dialog box that can be shown during image enumeration and acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8690c67b-5f96-4e8c-8685-91fe5ed65511">Destroy</a>
</td>
<td align="left" width="63%">
Closes and disposes of the progress dialog box shown during image enumeration and acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f797e68-f87d-4f90-853b-60c6c9309f58">GetUserInput</a>
</td>
<td align="left" width="63%">
Retrieves descriptive information entered by the user, such as the tag name of the images to store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c407e0a6-676f-419d-ab9a-85f5d0dcc480">GetWindow</a>
</td>
<td align="left" width="63%">
Retrieves the handle to the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bd84b1f-7a2a-40eb-ba77-21a8f701e5e0">IsCancelled</a>
</td>
<td align="left" width="63%">
Indicates whether the operation has been canceled via the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05810577-c23a-4f75-9cd5-0b5b6be7d181">IsCheckboxChecked</a>
</td>
<td align="left" width="63%">
Indicates whether the check box in the progress dialog box (typically indicating whether to delete files after transfer) is selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01689aa9-e3ae-48b4-b105-25880097a112">SetCaption</a>
</td>
<td align="left" width="63%">
Sets the caption of the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db516dcd-90b4-4421-b883-2f8462b36249">SetCheckboxText</a>
</td>
<td align="left" width="63%">
Sets the text for the check box in the progress dialog box indicating whether to delete images after transfer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88719891-9661-4766-adce-6b74cf9a87ef">SetCheckboxTooltip</a>
</td>
<td align="left" width="63%">
Sets the tooltip text for the check box in the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45b795c4-4f95-4132-86a7-cda47e534e9c">SetImage</a>
</td>
<td align="left" width="63%">
Sets either the thumbnail image displayed in the progress dialog box, the icon in the title bar of the progress dialog box, or the icon in ALT+TAB key combination windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2fb225d-6d2b-49f7-bbc9-715107e90df2">SetPercentComplete</a>
</td>
<td align="left" width="63%">
Sets a value indicating the completed portion of the current operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3210667-1fe2-4b30-9e5e-311f720647ce">SetProgressText</a>
</td>
<td align="left" width="63%">
Sets the text for the progress bar in the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee1f8b8e-bc46-4699-a682-2933c18a794b">SetTitle</a>
</td>
<td align="left" width="63%">
Sets the title of the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6518c073-b4d9-49df-819f-473028ad230a">ShowCheckbox</a>
</td>
<td align="left" width="63%">
Indicates whether to show the check box in the progress dialog box indicating whether to delete images after transfer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f58529da-f419-445a-879a-2c087b770f0f">Interfaces</a>
 

 

