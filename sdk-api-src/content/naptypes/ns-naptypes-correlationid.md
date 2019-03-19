---
UID: NS:naptypes.tagCorrelationId
title: CorrelationId (naptypes.h)
author: windows-sdk-content
description: Is used to pair SoHRequests with SoHResponses and uniquely describes an SoH exchange.
old-location: nap\correlationid_struct.htm
tech.root: NAP
ms.assetid: 99e5bad8-47dd-447b-bd8d-e35ae765808b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CorrelationId, CorrelationId structure [NAP], nap.correlationid_struct, naptypes/CorrelationId
ms.topic: struct
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
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
 - NapTypes.h
api_name:
 - CorrelationId
product: Windows
targetos: Windows
req.typenames: CorrelationId
req.redist: 
---

# CorrelationId structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>CorrelationId</b> structure is used to pair <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoHRequests</a> with <b>SoHResponses</b> and uniquely describes an SoH exchange.


## -struct-fields




### -field connId

A globally unique identifier (GUID) that identifies a SoH  exchange.


### -field timeStamp

A  unique <a href="http://go.microsoft.com/fwlink/p/?linkid=90006">FILETIME</a> value that contains the system time at which the <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoHRequest</a> was generated. 


## -remarks



The
   string version, <a href="https://msdn.microsoft.com/54f2866b-4333-4fc8-bb25-b7d4ae72b7dc">StringCorrelationId</a>, is used primarily for logging purposes,
   whereas this byte version is used by SHA/SHVs to
   match <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoHRequests</a> to <b>SoHResponses</b>.




## -see-also




<a href="https://msdn.microsoft.com/54f2866b-4333-4fc8-bb25-b7d4ae72b7dc">NAP Datatypes</a>



<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>
 

 

