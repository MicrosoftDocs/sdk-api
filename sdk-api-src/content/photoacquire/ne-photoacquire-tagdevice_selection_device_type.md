---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagDEVICE_SELECTION_DEVICE_TYPE enumeration


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



This enumeration type is pointed to by the <i>pnDeviceType</i> parameter of <a href="https://msdn.microsoft.com/eb79c07b-3b80-4f2b-b1f1-2394e1c7a30b">IPhotoAcquireDeviceSelectionDialog::DoModal</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/eb79c07b-3b80-4f2b-b1f1-2394e1c7a30b">IPhotoAcquireDeviceSelectionDialog::DoModal</a>
 

 

