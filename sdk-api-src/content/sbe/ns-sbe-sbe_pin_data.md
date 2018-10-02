---
UID: NS:sbe.SBE_PIN_DATA
title: SBE_PIN_DATA
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 2 only. The STREAMBUFFER_ATTRIBUTE structure contains performance data for the stream buffer filters.
old-location: mstv\sbe_pin_data.htm
tech.root: MSTV
ms.assetid: 727aa921-5156-4b7a-a184-b0744acfa6fb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SBE_PIN_DATA, SBE_PIN_DATA structure [Microsoft TV Technologies], SBE_PIN_DATAStructure, mstv.sbe_pin_data, sbe/SBE_PIN_DATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sbe.h
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
 - Sbe.h
api_name:
 - SBE_PIN_DATA
product: Windows
targetos: Windows
req.typenames: SBE_PIN_DATA
req.redist: 
---

# SBE_PIN_DATA structure


## -description



This topic applies to Windows XP Service Pack 2 only.
          

The <b>STREAMBUFFER_ATTRIBUTE</b> structure contains performance data for the stream buffer filters.




## -struct-fields




### -field cDataBytes

Total sample payload, in bytes.


### -field cSamplesProcessed

Number of samples processed.


### -field cDiscontinuities

Number of discontinuities. See <a href="https://msdn.microsoft.com/57041c71-4c7e-463a-92f5-c77a76aa545a">IMediaSample::SetDiscontinuity</a>.


### -field cSyncPoints

Number of synchronization points. See <a href="https://msdn.microsoft.com/b2770045-c18b-4dbc-b104-873e07c0b5aa">IMediaSample::SetSyncPoint</a>.


### -field cTimestamps

Number of time stamps.


## -see-also




<a href="https://msdn.microsoft.com/15895ff3-37e5-4f89-bcce-3b9f060c0746">IStreamBufferDataCounters::GetData</a>



<a href="https://msdn.microsoft.com/90ac310a-7fd3-440f-9cf7-7d6eb58996cc">Stream Buffer Engine Structures</a>
 

 

