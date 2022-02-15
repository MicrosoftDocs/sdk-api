---
UID: NF:srpapi.SrpDoesPolicyAllowAppExecution
title: SrpDoesPolicyAllowAppExecution function (srpapi.h)
description: Evaluates whether a packaged app will be allowed to execute based on software restriction policies.
helpviewer_keywords: ["EDP.srpdoespolicyallowappexecution_","SrpDoesPolicyAllowAppExecution","SrpDoesPolicyAllowAppExecution","SrpDoesPolicyAllowAppExecution function","srpapi/SrpDoesPolicyAllowAppExecution"]
old-location: edp\srpdoespolicyallowappexecution_.htm
tech.root: EDP
ms.assetid: 2649E719-2BF8-4AE6-B563-0230487A7BD2
ms.date: 12/05/2018
ms.keywords: EDP.srpdoespolicyallowappexecution_, SrpDoesPolicyAllowAppExecution, SrpDoesPolicyAllowAppExecution , SrpDoesPolicyAllowAppExecution function, srpapi/SrpDoesPolicyAllowAppExecution
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
 - SrpDoesPolicyAllowAppExecution
 - srpapi/SrpDoesPolicyAllowAppExecution
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
 - SrpDoesPolicyAllowAppExecution
---

# SrpDoesPolicyAllowAppExecution function


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Evaluates whether a packaged app will be allowed to execute based on software restriction policies.

## -parameters

### -param packageId [in]

Provides package name, publisher name, and version of the packaged app.

### -param isAllowed [out]

A boolean value that indicates whether the app is allowed to execute.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

