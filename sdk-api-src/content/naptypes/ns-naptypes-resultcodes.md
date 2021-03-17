---
UID: NS:naptypes.tagResultCodes
title: ResultCodes (naptypes.h)
description: Defines a list of result codes.
helpviewer_keywords: ["ResultCodes","ResultCodes structure [NAP]","nap.resultcodes_struct","naptypes/ResultCodes"]
old-location: nap\resultcodes_struct.htm
tech.root: NAP
ms.assetid: 9d608f0a-9841-48e6-8856-2d8c1afc3e5d
ms.date: 12/05/2018
ms.keywords: ResultCodes, ResultCodes structure [NAP], nap.resultcodes_struct, naptypes/ResultCodes
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
req.typenames: ResultCodes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagResultCodes
 - naptypes/tagResultCodes
 - ResultCodes
 - naptypes/ResultCodes
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
 - ResultCodes
---

# ResultCodes structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>ResultCodes</b> structure defines a list of result codes.

## -struct-fields

### -field count

The number of result codes as a number between 0 and <a href="/windows/desktop/NAP/nap-type-constants">maxDwordCountPerSoHAttribute</a>.

### -field results

A pointer to either a list of application defined 4-octet HRESULTs that specify whether the client machine is compliant, or a list of <a href="/windows/desktop/NAP/nap-error-constants">NAP error constants</a> that specify the cause of <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoH</a> construction or processing errors. The values must be in the byte ordering of the host system.

## -see-also

<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>