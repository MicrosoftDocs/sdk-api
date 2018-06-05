---
UID: NE:imapi2._IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE
title: "_IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE"
author: windows-sdk-content
description: Defines values that indicate the type of sub-channel data.
old-location: imapi\imapi_format2_raw_cd_data_sector_type.htm
old-project: imapi
ms.assetid: f3193377-5410-4cd2-b7e5-281b3794c583
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PIMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE, IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE, IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE enumeration [IMAPI], IMAPI_FORMAT2_RAW_CD_SUBCODE_IS_COOKED, IMAPI_FORMAT2_RAW_CD_SUBCODE_IS_RAW, IMAPI_FORMAT2_RAW_CD_SUBCODE_PQ_ONLY, PIMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE, PIMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE enumeration pointer [IMAPI], _IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE, imapi.imapi_format2_raw_cd_data_sector_type, imapi2/IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE, imapi2/IMAPI_FORMAT2_RAW_CD_SUBCODE_IS_COOKED, imapi2/IMAPI_FORMAT2_RAW_CD_SUBCODE_IS_RAW, imapi2/IMAPI_FORMAT2_RAW_CD_SUBCODE_PQ_ONLY, imapi2/PIMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE, *PIMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	imapi2.h
api_name:
-	IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

