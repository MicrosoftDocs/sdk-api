---
UID: NF:roerrorapi.RoReportFailedDelegate
title: RoReportFailedDelegate function
author: windows-sdk-content
description: Triggers the Global Error Handler when a delegate failure occurs.
old-location: winrt\roreportfaileddelegate.htm
old-project: WinRT
ms.assetid: 0A35A174-9020-438E-94CF-3A790D158144
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: RoReportFailedDelegate, RoReportFailedDelegate function [Windows Runtime], roerrorapi/RoReportFailedDelegate, winrt.roreportfaileddelegate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RuntimeObject.lib
-	RuntimeObject.dll
-	API-MS-Win-Core-WinRT-error-l1-1-1.dll
-	COMBase.dll
api_name:
-	RoReportFailedDelegate
product: Windows
targetos: Windows
req.lib: RuntimeObject.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RoReportFailedDelegate function


## -description


Triggers the Global Error Handler when a delegate failure occurs.


## -parameters




### -param punkDelegate [in]

The delegate to report.


### -param pRestrictedErrorInfo [in]

The error to report. Call the <a href="https://msdn.microsoft.com/CA459E57-90D5-44F6-A896-4E1C2FA0DC57">GetRestrictedErrorInfo</a> function to get the <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> that represents the error.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



