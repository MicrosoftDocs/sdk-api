---
UID: NF:photoacquire.IPhotoAcquireDeviceSelectionDialog.DoModal
title: IPhotoAcquireDeviceSelectionDialog::DoModal
author: windows-sdk-content
description: The DoModal method displays a device selection dialog box. The function returns when the user selects a device using the modal dialog box.
old-location: picacq\iphotoacquiredeviceselectiondialog_domodal.htm
tech.root: acquisition
ms.assetid: eb79c07b-3b80-4f2b-b1f1-2394e1c7a30b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DoModal, DoModal method [Picture Acquisition], DoModal method [Picture Acquisition],IPhotoAcquireDeviceSelectionDialog interface, IPhotoAcquireDeviceSelectionDialog interface [Picture Acquisition],DoModal method, IPhotoAcquireDeviceSelectionDialog.DoModal, IPhotoAcquireDeviceSelectionDialog::DoModal, IPhotoAcquireDeviceSelectionDialogDoModal, photoacquire/IPhotoAcquireDeviceSelectionDialog::DoModal, picacq.iphotoacquiredeviceselectiondialog_domodal
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
 - IPhotoAcquireDeviceSelectionDialog.DoModal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireDeviceSelectionDialog::DoModal


## -description



The <code>DoModal</code> method displays a device selection dialog box. The function returns when the user selects a device using the modal dialog box.




## -parameters




### -param hWndParent [in]

Handle to a parent window.


### -param dwDeviceFlags [in]

Double word value containing a combination of device flags that indicate which type of devices to display. The device flags may be a combination of any of the following:

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>DSF_WPD_DEVICES</b></td>
<td>Show devices of type Windows Portable Devices (WPD).</td>
</tr>
<tr>
<td><b>DSF_WIA_CAMERAS</b></td>
<td>Show cameras of type Windows Image Acquisition (WIA).</td>
</tr>
<tr>
<td><b>DSF_WIA_SCANNERS</b></td>
<td>Show scanners of type Windows Image Acquisition (WIA).</td>
</tr>
<tr>
<td><b>DSF_STI_DEVICES</b></td>
<td>Show devices of type Still Image Architecture (STI).</td>
</tr>
<tr>
<td><b>DSF_FS_DEVICES</b></td>
<td>Show removable storage devices, such as CD drives or card readers.</td>
</tr>
<tr>
<td><b>DSF_DV_DEVICES</b></td>
<td>Show digital video camera devices.</td>
</tr>
<tr>
<td><b>DSF_ALL_DEVICES</b></td>
<td>Show all devices.</td>
</tr>
<tr>
<td><b>DSF_SHOW_OFFLINE</b></td>
<td>Show devices that are offline. Not supported by all device types.</td>
</tr>
</table>
 




### -param pbstrDeviceId [out]

Pointer to a string containing the ID of the selected device.


### -param pnDeviceType [out]

Pointer to the <a href="https://msdn.microsoft.com/95f528d1-ff83-4d42-9050-b137476935b0">DEVICE_SELECTION_DEVICE_TYPE</a> of the selected device.


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




<a href="https://msdn.microsoft.com/95f528d1-ff83-4d42-9050-b137476935b0">DEVICE_SELECTION_DEVICE_TYPE</a>



<a href="https://msdn.microsoft.com/7ec649d2-9fd7-4c07-ad64-f3bc4acfc40d">IPhotoAcquireDeviceSelectionDialog Interface</a>
 

 

