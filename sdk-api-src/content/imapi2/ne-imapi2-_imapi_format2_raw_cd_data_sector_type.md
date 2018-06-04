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

# _IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE enumeration


## -description


Defines values that indicate the type of sub-channel data.


## -enum-fields




### -field IMAPI_FORMAT2_RAW_CD_SUBCODE_PQ_ONLY

The data contains P and Q sub-channel data.


### -field IMAPI_FORMAT2_RAW_CD_SUBCODE_IS_COOKED

The data contains corrected and de-interleaved R-W sub-channel data. 


### -field IMAPI_FORMAT2_RAW_CD_SUBCODE_IS_RAW

The data contains raw P-W sub-channel data that is returned in the order received from the disc surface. 


## -remarks



For details on the format of the sub-channel data, see Sub-Channel Field Formats in the latest release of the MMC specification at <a href="Http://go.microsoft.com/fwlink/p/?linkid=83843">ftp://ftp.t10.org/t10/drafts/mmc5</a>.




## -see-also




<a href="https://msdn.microsoft.com/d217e585-3ff4-4f02-8a13-7cfca767f201">IDiscFormat2RawCD::get_SupportedSectorTypes</a>
 

 

