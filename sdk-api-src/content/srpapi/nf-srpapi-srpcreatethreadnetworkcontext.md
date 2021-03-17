---
UID: NF:srpapi.SrpCreateThreadNetworkContext
title: SrpCreateThreadNetworkContext function (srpapi.h)
description: Sets the enterprise ID as the data context of the current thread. This is allowed only if the process already has the same enterprise ID present in its process context. It optionally returns the existing thread token.
helpviewer_keywords: ["EDP.srpcreatethreadnetworkcontext","SrpCreateThreadNetworkContext","SrpCreateThreadNetworkContext function","srpapi/SrpCreateThreadNetworkContext"]
old-location: edp\srpcreatethreadnetworkcontext.htm
tech.root: EDP
ms.assetid: 95997D25-04FE-445B-ADC1-DE85A34BD70C
ms.date: 12/05/2018
ms.keywords: EDP.srpcreatethreadnetworkcontext, SrpCreateThreadNetworkContext, SrpCreateThreadNetworkContext function, srpapi/SrpCreateThreadNetworkContext
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
 - SrpCreateThreadNetworkContext
 - srpapi/SrpCreateThreadNetworkContext
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
 - SrpCreateThreadNetworkContext
---

# SrpCreateThreadNetworkContext function


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Sets the enterprise ID as the data context of the current thread. This is allowed only if the process already has the same enterprise ID present in its process context. It optionally returns the existing thread token.

## -parameters

### -param enterpriseId [in]

The enterprise ID to set in the current thread's token.

### -param threadNetworkContext [out]

On success, holds the existing thread token.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

