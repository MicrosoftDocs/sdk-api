---
UID: NA:diagnosticdataquery
title: diagnosticdataquery
ms.date: 8/19/2019
ms.keywords: diagnosticdataquery
description: 
ms.localizationpriority: high
tech.root: security
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: apiset
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquery.h
api_name:
 - diagnosticdataquery
f1_keywords:
 - diagnosticdataquery
 - diagnosticdataquery/diagnosticdataquery
---

## -description

The DiagnosticDataQuery (DDQ) API allows queries for diagnostic data events uploaded from a Windows machine by the Connected User Experiences and Telemetry service. It also allows access to the error reports uploaded by Windows Error Reporting. 

WinRT apps are required to have the telemetry data capability to use the DDQ API. This capability is restricted only to first party applications. Unless your application is specially provisioned to have this capability, calls to some of these APIs will fail at runtime.

## -remarks

## -see-also
