---
UID: NE:photoacquire.tagDEVICE_SELECTION_DEVICE_TYPE
title: DEVICE_SELECTION_DEVICE_TYPE (photoacquire.h)
description: The DEVICE_SELECTION_DEVICE_TYPE enumeration type indicates the type of a selected device.
helpviewer_keywords: ["DEVICE_SELECTION_DEVICE_TYPE","DEVICE_SELECTION_DEVICE_TYPE enumeration [Picture Acquisition]","DSF_TWAIN_DEVICE","DST_FS_DEVICE","DST_STI_DEVICE","DST_UNKNOWN_DEVICE","DST_WIA_DEVICE","DST_WPD_DEVICE","enumeration [Picture Acquisition]","photoacquire/DEVICE_SELECTION_DEVICE_TYPE","photoacquire/DSF_TWAIN_DEVICE","photoacquire/DST_FS_DEVICE","photoacquire/DST_STI_DEVICE","photoacquire/DST_UNKNOWN_DEVICE","photoacquire/DST_WIA_DEVICE","photoacquire/DST_WPD_DEVICE","picacq.device_selection_device_type"]
old-location: picacq\device_selection_device_type.htm
tech.root: picacq
ms.assetid: 95f528d1-ff83-4d42-9050-b137476935b0
ms.date: 12/05/2018
ms.keywords: DEVICE_SELECTION_DEVICE_TYPE, DEVICE_SELECTION_DEVICE_TYPE enumeration [Picture Acquisition], DSF_TWAIN_DEVICE, DST_FS_DEVICE, DST_STI_DEVICE, DST_UNKNOWN_DEVICE, DST_WIA_DEVICE, DST_WPD_DEVICE, enumeration [Picture Acquisition], photoacquire/DEVICE_SELECTION_DEVICE_TYPE, photoacquire/DSF_TWAIN_DEVICE, photoacquire/DST_FS_DEVICE, photoacquire/DST_STI_DEVICE, photoacquire/DST_UNKNOWN_DEVICE, photoacquire/DST_WIA_DEVICE, photoacquire/DST_WPD_DEVICE, picacq.device_selection_device_type
f1_keywords:
- photoacquire/DEVICE_SELECTION_DEVICE_TYPE
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
- HeaderDef
api_location:
- PhotoAcquire.h
api_name:
- DEVICE_SELECTION_DEVICE_TYPE
targetos: Windows
req.typenames: DEVICE_SELECTION_DEVICE_TYPE
req.redist: 
ms.custom: 19H1
---

# DEVICE_SELECTION_DEVICE_TYPE enumeration


## -description



The <code>DEVICE_SELECTION_DEVICE_TYPE</code> enumeration type indicates the type of a selected device.




## -enum-fields




### -field DST_UNKNOWN_DEVICE

Specifies that the type of the selected device is unknown.


### -field DST_WPD_DEVICE

Specifies that the type of the selected device is Windows Portable Devices (WPD).


### -field DST_WIA_DEVICE

Specifies that the type of the selected device is Windows Image Acquisition (WIA).


### -field DST_STI_DEVICE

Specifies that the type of the selected device is Still Image Architecture (STI).


### -field DSF_TWAIN_DEVICE

Not supported.


### -field DST_FS_DEVICE

Specifies that the selected device is a removable drive in the file system.


### -field DST_DV_DEVICE




## -remarks



This enumeration type is pointed to by the <i>pnDeviceType</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiredeviceselectiondialog-domodal">IPhotoAcquireDeviceSelectionDialog::DoModal</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/enumeration-types">Enumeration Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiredeviceselectiondialog-domodal">IPhotoAcquireDeviceSelectionDialog::DoModal</a>
 

 

