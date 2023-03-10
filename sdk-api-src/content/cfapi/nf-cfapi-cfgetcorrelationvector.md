---
UID: NF:cfapi.CfGetCorrelationVector
title: CfGetCorrelationVector function (cfapi.h)
description: Allows the sync provider to query the current correlation vector for a given placeholder file.
helpviewer_keywords: ["CfGetCorrelationVector","CfGetCorrelationVector function","cfapi/CfGetCorrelationVector","cloudApi.cfgetcorrelationvector"]
old-location: cloudapi\cfgetcorrelationvector.htm
tech.root: cloudapi
ms.assetid: 3DB0AAFE-82DC-4707-8DB6-C52D4A9B2771
ms.date: 12/05/2018
ms.keywords: CfGetCorrelationVector, CfGetCorrelationVector function, cfapi/CfGetCorrelationVector, cloudApi.cfgetcorrelationvector
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
 - CfGetCorrelationVector
 - cfapi/CfGetCorrelationVector
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
 - CfGetCorrelationVector
---

# CfGetCorrelationVector function


## -description

Allows the sync provider to query the current correlation vector for a given placeholder file.

## -parameters

### -param FileHandle [in]

The handle to the placeholder file.

### -param CorrelationVector [out]

The correlation vector for the <i>FileHandle</i>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

