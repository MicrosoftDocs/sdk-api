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

# _WIA_EXTENDED_TRANSFER_INFO structure


## -description


The <b>WIA_EXTENDED_TRANSFER_INFO</b> structure specifies extended transfer information for the <a href="https://msdn.microsoft.com/268a5c3e-2717-40c3-9f24-cc490b1e593b">IWiaDataTransfer::idtGetExtendedTransferInfo</a> method.


## -struct-fields




### -field ulSize

Type: <b>ULONG</b>

Size of this structure.



### -field ulMinBufferSize

Type: <b>ULONG</b>

Minimum buffer size the application should request in a call to <a href="https://msdn.microsoft.com/3cbef4c0-cf28-4fdd-b347-84428ffd671b">IWiaDataTransfer::idtGetBandedData</a>.


### -field ulOptimalBufferSize

Type: <b>ULONG</b>

Driver-recommended buffer size the application should request in a call to <a href="https://msdn.microsoft.com/3cbef4c0-cf28-4fdd-b347-84428ffd671b">IWiaDataTransfer::idtGetBandedData</a>.


### -field ulMaxBufferSize

Type: <b>ULONG</b>

Driver-recommended maximum buffer size the application could request in a call to <a href="https://msdn.microsoft.com/3cbef4c0-cf28-4fdd-b347-84428ffd671b">IWiaDataTransfer::idtGetBandedData</a>. Going over this limit is not detrimental, however, the driver can simply not use the whole buffer and limit each band of data to this maximum size.


### -field ulNumBuffers

Type: <b>ULONG</b>

This value is not used and should be ignored.

