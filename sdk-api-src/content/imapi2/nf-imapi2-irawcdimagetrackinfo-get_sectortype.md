---
UID: NF:imapi2.IRawCDImageTrackInfo.get_SectorType
title: IRawCDImageTrackInfo::get_SectorType
author: windows-driver-content
description: Retrieves the type of data provided for the sectors in this track. For more detail on the possible sector types, see IMAPI_CD_SECTOR_TYPE.
old-location: imapi\irawcdimagetrackinfo_get_sectortype.htm
old-project: imapi
ms.assetid: fbec6c4b-dd0e-46c3-9e46-97b8f98438b3
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],get_SectorType method, IRawCDImageTrackInfo.get_SectorType, IRawCDImageTrackInfo::get_SectorType, get_SectorType, get_SectorType method [IMAPI], get_SectorType method [IMAPI],IRawCDImageTrackInfo interface, imapi.irawcdimagetrackinfo_get_sectortype, imapi2/IRawCDImageTrackInfo::get_SectorType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IRawCDImageTrackInfo.get_SectorType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IRawCDImageTrackInfo::get_SectorType


## -description


Retrieves the type of data provided for the sectors in this track. For more detail on the possible sector types, see <a href="https://msdn.microsoft.com/3af4a8c9-66b7-490e-aafa-fdfe614f5f3e">IMAPI_CD_SECTOR_TYPE</a>.


## -parameters




### -param value [out]

A pointer to a <a href="https://msdn.microsoft.com/3af4a8c9-66b7-490e-aafa-fdfe614f5f3e">IMAPI_CD_SECTOR_TYPE</a> enumeration that specifies the type of data provided for the sectors on the track. 


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/3af4a8c9-66b7-490e-aafa-fdfe614f5f3e">IMAPI_CD_SECTOR_TYPE</a>



<a href="https://msdn.microsoft.com/5d074279-35fb-48d0-b298-c1a83f57d805">IRawCDImageTrackInfo</a>
 

 

