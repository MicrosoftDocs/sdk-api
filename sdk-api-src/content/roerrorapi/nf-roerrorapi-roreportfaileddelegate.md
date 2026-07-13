---
UID: NF:roerrorapi.RoReportFailedDelegate
title: RoReportFailedDelegate function
description: Triggers the Global Error Handler when a delegate failure occurs.
helpviewer_keywords: ["RoReportFailedDelegate","RoReportFailedDelegate function [Windows Runtime]","roerrorapi/RoReportFailedDelegate","winrt.roreportfaileddelegate"]
old-location: winrt\roreportfaileddelegate.htm
tech.root: WinRT
ms.assetid: 0A35A174-9020-438E-94CF-3A790D158144
ms.date: 12/5/2018
ms.keywords: RoReportFailedDelegate, RoReportFailedDelegate function [Windows Runtime], roerrorapi/RoReportFailedDelegate, winrt.roreportfaileddelegate
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - RoReportFailedDelegate
 - roerrorapi/RoReportFailedDelegate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RuntimeObject.lib
 - RuntimeObject.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
 - COMBase.dll
api_name:
 - RoReportFailedDelegate
---

# RoReportFailedDelegate function


## -description

Triggers the Global Error Handler when a delegate failure occurs.

## -parameters

### -param punkDelegate [in]

The delegate to report.

### -param pRestrictedErrorInfo [in]

The error to report. Call the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo">GetRestrictedErrorInfo</a> function to get the <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> that represents the error.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.