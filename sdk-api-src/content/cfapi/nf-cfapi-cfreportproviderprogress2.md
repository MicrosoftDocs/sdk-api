---
UID: NF:cfapi.CfReportProviderProgress2
tech.root: cloudapi
title: CfReportProviderProgress2
ms.date: 03/30/2023
targetos: Windows
description: Allows a sync provider to report progress out-of-band. Extends CfReportProviderProgress with additional parameters.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cfapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: cldapi.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1809 (10.0; Build 17763)
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - cfapi.h
api_name:
 - CfReportProviderProgress2
f1_keywords:
 - CfReportProviderProgress2
 - cfapi/CfReportProviderProgress2
dev_langs:
 - c++
---

## -description

Allows a sync provider to report progress out-of-band. Extends [CfReportProviderProgress](nf-cfapi-cfreportproviderprogress.md) with additional parameters.

## -parameters

### -param ConnectionKey

A connection key representing a communication channel with the sync filter.

### -param TransferKey

An opaque handle to the placeholder.

### -param RequestKey

Allows the caller to report progress on a specific operation other than hydration.

### -param ProviderProgressTotal

The total progress of the sync provider in response to a fetch data callback.

### -param ProviderProgressCompleted

The completed progress of the sync provider in response to a fetch data callback.

### -param TargetSessionId

Indicates the session at which this progress information is targeted.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also

[CfReportProviderProgress](nf-cfapi-cfreportproviderprogress.md)
