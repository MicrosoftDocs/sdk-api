---
UID: NS:wmpdevices._WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
title: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
author: windows-sdk-content
description: The WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE structure is used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.
old-location: wmp\wmp_wmdm_metadata_round_trip_pc2device.htm
tech.root: WMP
ms.assetid: 825d4080-45de-452e-b0eb-33e7bd1d2f22
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE, WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE structure [Windows Media Player], WMP_WMDM_PC2DEVICE, wmp.wmp_wmdm_metadata_round_trip_pc2device, wmpdevices/WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wmpdevices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
 - wmpdevices.h
api_name:
 - WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
product: Windows
targetos: Windows
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
req.redist: 
---

# WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE structure


## -description


The <b>WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE</b> structure is used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.


## -struct-fields




### -field dwChangesSinceTransactionID

The transaction identifier supplied by the device during the previous session. This value is zero for the first session ever.


### -field dwResultSetStartingIndex

The index of the first value to retrieve. This value is always zero for the first call of a session.


## -see-also




<a href="https://msdn.microsoft.com/c1d84225-b5b1-4f9e-8694-a229653e53de">Windows Media Device Manager Device Extensions for Metadata Transfer</a>
 

 

