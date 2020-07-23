---
UID: NN:photoacquire.IPhotoProgressDialog
title: IPhotoProgressDialog (photoacquire.h)
description: Provides the progress dialog box that may be displayed when enumerating or importing images. The dialog box is modal and runs in its own thread.
helpviewer_keywords: ["IPhotoProgressDialog","IPhotoProgressDialog interface [Picture Acquisition]","IPhotoProgressDialog interface [Picture Acquisition]","described","IPhotoProgressDialogInterface","photoacquire/IPhotoProgressDialog","picacq.iphotoprogressdialog"]
old-location: picacq\iphotoprogressdialog.htm
tech.root: picacq
ms.assetid: a3928874-5a15-43d9-9d9c-8b66478b0597
ms.date: 12/05/2018
ms.keywords: IPhotoProgressDialog, IPhotoProgressDialog interface [Picture Acquisition], IPhotoProgressDialog interface [Picture Acquisition],described, IPhotoProgressDialogInterface, photoacquire/IPhotoProgressDialog, picacq.iphotoprogressdialog
f1_keywords:
- photoacquire/IPhotoProgressDialog
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
- IPhotoProgressDialog
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoProgressDialog interface


## -description



Provides the progress dialog box that may be displayed when enumerating or importing images. The dialog box is modal and runs in its own thread.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoProgressDialog</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhotoProgressDialog</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-create">Create</a>
</td>
<td align="left" width="63%">
Creates and displays a progress dialog box that can be shown during image enumeration and acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-destroy">Destroy</a>
</td>
<td align="left" width="63%">
Closes and disposes of the progress dialog box shown during image enumeration and acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-getuserinput">GetUserInput</a>
</td>
<td align="left" width="63%">
Retrieves descriptive information entered by the user, such as the tag name of the images to store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-getwindow">GetWindow</a>
</td>
<td align="left" width="63%">
Retrieves the handle to the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-iscancelled">IsCancelled</a>
</td>
<td align="left" width="63%">
Indicates whether the operation has been canceled via the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-ischeckboxchecked">IsCheckboxChecked</a>
</td>
<td align="left" width="63%">
Indicates whether the check box in the progress dialog box (typically indicating whether to delete files after transfer) is selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-setcaption">SetCaption</a>
</td>
<td align="left" width="63%">
Sets the caption of the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-setcheckboxtext">SetCheckboxText</a>
</td>
<td align="left" width="63%">
Sets the text for the check box in the progress dialog box indicating whether to delete images after transfer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-setcheckboxtooltip">SetCheckboxTooltip</a>
</td>
<td align="left" width="63%">
Sets the tooltip text for the check box in the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-setimage">SetImage</a>
</td>
<td align="left" width="63%">
Sets either the thumbnail image displayed in the progress dialog box, the icon in the title bar of the progress dialog box, or the icon in ALT+TAB key combination windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-setpercentcomplete">SetPercentComplete</a>
</td>
<td align="left" width="63%">
Sets a value indicating the completed portion of the current operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-setprogresstext">SetProgressText</a>
</td>
<td align="left" width="63%">
Sets the text for the progress bar in the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-settitle">SetTitle</a>
</td>
<td align="left" width="63%">
Sets the title of the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-showcheckbox">ShowCheckbox</a>
</td>
<td align="left" width="63%">
Indicates whether to show the check box in the progress dialog box indicating whether to delete images after transfer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/interfaces">Interfaces</a>
 

 

