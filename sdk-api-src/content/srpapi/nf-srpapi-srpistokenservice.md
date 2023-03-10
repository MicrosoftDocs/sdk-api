---
UID: NF:srpapi.SrpIsTokenService
title: SrpIsTokenService function (srpapi.h)
description: Identifies whether a service is a token service.
helpviewer_keywords: ["EDP.srpistokenservice","SrpIsTokenService","SrpIsTokenService function","srpapi/SrpIsTokenService"]
old-location: edp\srpistokenservice.htm
tech.root: EDP
ms.assetid: 5049B594-A882-49F0-A18B-6A28818AD8D2
ms.date: 12/05/2018
ms.keywords: EDP.srpistokenservice, SrpIsTokenService, SrpIsTokenService function, srpapi/SrpIsTokenService
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
 - SrpIsTokenService
 - srpapi/SrpIsTokenService
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
 - SrpIsTokenService
---

# SrpIsTokenService function


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy cannot be applied on Windows 10, version 1511 (build 10586) or earlier.</div>
<div> </div>Identifies whether a service is a token service.

## -parameters

### -param TokenHandle [in]

Token Handle to be checked.

### -param IsTokenService [out]

A boolean value that indicates whether the service is a token service.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

