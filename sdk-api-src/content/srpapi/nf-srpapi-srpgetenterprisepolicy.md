---
UID: NF:srpapi.SrpGetEnterprisePolicy
title: SrpGetEnterprisePolicy function (srpapi.h)
description: Policy can be applied on Windows 10, version 1607.Gets information about the enterprise policy of an app.
helpviewer_keywords: ["EDP.srpgetenterprisepolicy","SrpGetEnterprisePolicy","SrpGetEnterprisePolicy function","srpapi/SrpGetEnterprisePolicy"]
old-location: edp\srpgetenterprisepolicy.htm
tech.root: EDP
ms.assetid: BF31E36C-756E-4B4A-959B-4BA7517427CB
ms.date: 12/05/2018
ms.keywords: EDP.srpgetenterprisepolicy, SrpGetEnterprisePolicy, SrpGetEnterprisePolicy function, srpapi/SrpGetEnterprisePolicy
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
 - SrpGetEnterprisePolicy
 - srpapi/SrpGetEnterprisePolicy
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
 - SrpGetEnterprisePolicy
---

# SrpGetEnterprisePolicy function


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Gets information about the enterprise policy of an app.

## -parameters

### -param tokenHandle [in]

Token Handle to be checked.

### -param policyFlags [out]

A collection of flags that indicate among other things whether the host app is allowed by the managing enterprise policy, and has been enlightened for Windows Information Protection.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

