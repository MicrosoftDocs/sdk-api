---
UID: NF:srpapi.SrpGetEnterpriseIds
title: SrpGetEnterpriseIds function (srpapi.h)
description: Gets the list of enterprise identifiers for the given token.
helpviewer_keywords: ["EDP.srpgetenterpriseids","SrpGetEnterpriseIds","SrpGetEnterpriseIds function","srpapi/SrpGetEnterpriseIds"]
old-location: edp\srpgetenterpriseids.htm
tech.root: EDP
ms.assetid: 850FA83D-A90F-40CA-99BE-F6DD890F4E6F
ms.date: 12/05/2018
ms.keywords: EDP.srpgetenterpriseids, SrpGetEnterpriseIds, SrpGetEnterpriseIds function, srpapi/SrpGetEnterpriseIds
req.header: srpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Srpapi.lib
req.dll: Srpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SrpGetEnterpriseIds
 - srpapi/SrpGetEnterpriseIds
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - srpapi.dll
 - Ext-MS-Win-Security-Srp-L1-1-0.dll
 - Ext-MS-Win-Security-Srp-L1-1-1.dll
api_name:
 - SrpGetEnterpriseIds
---

# SrpGetEnterpriseIds function


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy cannot be applied on Windows 10, version 1511 (build 10586) or earlier.</div>
<div> </div>Gets the list of enterprise identifiers for the given token.

The enterprise IDs are returned only for those applications explicitly allowed by management.

## -parameters

### -param tokenHandle [in]

Token Handle to be checked.

### -param numberOfBytes [in, out, optional]

If <i>enterpriseIds</i> is provided, then this supplies the size of the <i>enterpriseIds</i> buffer. If you provide a buffer size, and it's too small, the output will contain the required size of the <i>enterpriseIds</i> buffer.

### -param enterpriseIds [out, optional]

An array of enterprise ID string pointers.

### -param enterpriseIdCount [out]

The enterprise ID count on the token. Zero if the token is not explicitly enterprise allowed.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

If this function does not provide any enterprise IDs, it returns <b>E_NOT_SUFFICIENT_BUFFER</b>.

