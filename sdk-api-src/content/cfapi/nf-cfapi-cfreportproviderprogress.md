---
UID: NF:cfapi.CfReportProviderProgress
title: CfReportProviderProgress function (cfapi.h)
description: Allows a sync provider to report progress out-of-band.
helpviewer_keywords: ["CfReportProviderProgress","CfReportProviderProgress function","cfapi/CfReportProviderProgress","cloudApi.cfreportproviderprogress"]
old-location: cloudapi\cfreportproviderprogress.htm
tech.root: cloudapi
ms.assetid: 33AB46FD-200E-40FF-B061-5842C6433069
ms.date: 03/30/2023
ms.keywords: CfReportProviderProgress, CfReportProviderProgress function, cfapi/CfReportProviderProgress, cloudApi.cfreportproviderprogress
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
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
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfReportProviderProgress
 - cfapi/CfReportProviderProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfReportProviderProgress
---

# CfReportProviderProgress function

## -description

Allows a sync provider to report progress out-of-band.

## -parameters

### -param ConnectionKey [in]

A connection key representing a communication channel with the sync filter.

### -param TransferKey [in]

An opaque handle to the placeholder.

### -param ProviderProgressTotal [in]

The total progress of the sync provider in response to a fetch data callback.

### -param ProviderProgressCompleted [in]

The completed progress of the sync provider in response to a fetch data callback.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

The filter automatically tracks the progress of hydrations, by tracking ranges that are transferred and/or acknowledged in response to **FETCH_DATA** callbacks. However, if a provider spends the bulk of its time downloading content to a temporary location before beginning to **TRANSFER_DATA** to the filter, the filter would otherwise be unaware that these activities are in any way related to the request.

By calling **CfReportProviderProgress** periodically, the sync provider can report progress to the filter, thereby resetting the 60 second timeout period corresponding to the **CF_CALLBACK_TYPE_FETCH_DATA** callback. This will also make the progress appear smoother.

## -see-also

[CfReportProviderProgress2](nf-cfapi-cfreportproviderprogress2.md)

[CF_CALLBACK_TYPE](ne-cfapi-cf_callback_type.md)
