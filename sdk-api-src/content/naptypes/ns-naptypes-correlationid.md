---
UID: NS:naptypes.tagCorrelationId
title: CorrelationId (naptypes.h)
description: Is used to pair SoHRequests with SoHResponses and uniquely describes an SoH exchange.
helpviewer_keywords: ["CorrelationId","CorrelationId structure [NAP]","nap.correlationid_struct","naptypes/CorrelationId"]
old-location: nap\correlationid_struct.htm
tech.root: NAP
ms.assetid: 99e5bad8-47dd-447b-bd8d-e35ae765808b
ms.date: 12/05/2018
ms.keywords: CorrelationId, CorrelationId structure [NAP], nap.correlationid_struct, naptypes/CorrelationId
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
targetos: Windows
req.typenames: CorrelationId
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCorrelationId
 - naptypes/tagCorrelationId
 - CorrelationId
 - naptypes/CorrelationId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - CorrelationId
---

# CorrelationId structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>CorrelationId</b> structure is used to pair <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoHRequests</a> with <b>SoHResponses</b> and uniquely describes an SoH exchange.

## -struct-fields

### -field connId

A globally unique identifier (GUID) that identifies a SoH  exchange.

### -field timeStamp

A  unique <a href="/windows/win32/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> value that contains the system time at which the <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoHRequest</a> was generated.

## -remarks

The
   string version, <a href="/windows/desktop/NAP/nap-datatypes">StringCorrelationId</a>, is used primarily for logging purposes,
   whereas this byte version is used by SHA/SHVs to
   match <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoHRequests</a> to <b>SoHResponses</b>.

## -see-also

<a href="/windows/desktop/NAP/nap-datatypes">NAP Datatypes</a>



<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>