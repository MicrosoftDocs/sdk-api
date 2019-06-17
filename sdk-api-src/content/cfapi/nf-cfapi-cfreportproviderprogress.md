---
UID: NF:cfapi.CfReportProviderProgress
title: CfReportProviderProgress function (cfapi.h)
author: windows-sdk-content
description: Allows a sync provider to report progress out-of-band.
old-location: cloudapi\cfreportproviderprogress.htm
tech.root: cfApi
ms.assetid: 33AB46FD-200E-40FF-B061-5842C6433069
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CfReportProviderProgress, CfReportProviderProgress function, cfapi/CfReportProviderProgress, cloudApi.cfreportproviderprogress
ms.topic: function
f1_keywords: ["cfapi/CfReportProviderProgress"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfReportProviderProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



