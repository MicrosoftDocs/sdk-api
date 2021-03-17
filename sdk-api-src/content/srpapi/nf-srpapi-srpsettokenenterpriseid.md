---
UID: NF:srpapi.SrpSetTokenEnterpriseId
title: SrpSetTokenEnterpriseId function (srpapi.h)
description: Sets a data intent on a token. The caller process should be enterprise allowed for the provided enterprise ID.
helpviewer_keywords: ["EDP.srpsettokenenterpriseid","SrpSetTokenEnterpriseId","SrpSetTokenEnterpriseId function","srpapi/SrpSetTokenEnterpriseId"]
old-location: edp\srpsettokenenterpriseid.htm
tech.root: EDP
ms.assetid: A96E6977-5637-4E3E-A2AE-7892DC61FB08
ms.date: 12/05/2018
ms.keywords: EDP.srpsettokenenterpriseid, SrpSetTokenEnterpriseId, SrpSetTokenEnterpriseId function, srpapi/SrpSetTokenEnterpriseId
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
 - SrpSetTokenEnterpriseId
 - srpapi/SrpSetTokenEnterpriseId
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
 - SrpSetTokenEnterpriseId
---

# SrpSetTokenEnterpriseId function


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Sets a data intent on a token. The caller process should be enterprise allowed for the provided enterprise ID. 

If the caller intends to set a personal intent on the token, then NULL should be passed as enterprise ID.

## -parameters

### -param tokenHandle [in]

The token handle on which the intent is to be set.

### -param enterpriseId [in, optional]

The enterprise ID to set as intent.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

