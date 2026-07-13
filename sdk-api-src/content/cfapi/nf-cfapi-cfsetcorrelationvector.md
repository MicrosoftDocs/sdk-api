---
UID: NF:cfapi.CfSetCorrelationVector
title: CfSetCorrelationVector function (cfapi.h)
description: Allows a sync provider to instruct the platform to use a specific correlation vector for telemetry purposes on a placeholder file. This is optional.
helpviewer_keywords: ["CfSetCorrelationVector","CfSetCorrelationVector function","cfapi/CfSetCorrelationVector","cloudApi.cfsetcorrelationvector"]
old-location: cloudapi\cfsetcorrelationvector.htm
tech.root: cloudapi
ms.assetid: B9B05D24-BEE5-4BE6-95D5-C28466D69543
ms.date: 03/31/2023
ms.keywords: CfSetCorrelationVector, CfSetCorrelationVector function, cfapi/CfSetCorrelationVector, cloudApi.cfsetcorrelationvector
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
 - CfSetCorrelationVector
 - cfapi/CfSetCorrelationVector
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
 - CfSetCorrelationVector
---

# CfSetCorrelationVector function

## -description

Allows a sync provider to instruct the platform to use a specific correlation vector for telemetry purposes on a placeholder file. This is optional.

## -parameters

### -param FileHandle [in]

The handle to the placeholder file. The platform properly synchronizes the operation with other active requests. An attribute or no-access handle is sufficient.

### -param CorrelationVector [in]

A specific correlation vector to be associated with the *FileHandle*.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

The platform automatically assigns a correlation vector to each file when it is first opened, and provides this correlation vector with each callback to the sync provider as part of the common [CF_CALLBACK_INFO](ns-cfapi-cf_callback_info.md). It is suggested that the sync engine call this function to increment the last digit of the correlation vector “clock” as the sync provider progresses through internal stages (as defined by the sync provider) of satisfying the request.

## -see-also

[CF_CALLBACK_INFO](ns-cfapi-cf_callback_info.md)
