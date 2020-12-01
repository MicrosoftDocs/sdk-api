---
UID: NF:frquery.CFrameworkQuery.GetRequiredProperties
title: CFrameworkQuery::GetRequiredProperties (frquery.h)
description: The GetRequiredProperties method returns a list of all of the properties specified in the SELECT statement of a query. It returns the properties from both the SELECT and WHERE clauses.
helpviewer_keywords: ["CFrameworkQuery interface [Windows Management Instrumentation]","GetRequiredProperties method","CFrameworkQuery.GetRequiredProperties","CFrameworkQuery::GetRequiredProperties","GetRequiredProperties","GetRequiredProperties method [Windows Management Instrumentation]","GetRequiredProperties method [Windows Management Instrumentation]","CFrameworkQuery interface","_hmm_cframeworkquery_getrequiredproperties","frquery/CFrameworkQuery::GetRequiredProperties","wmi.cframeworkquery_getrequiredproperties"]
old-location: wmi\cframeworkquery_getrequiredproperties.htm
tech.root: wmi
ms.assetid: cf02aa01-6d56-4fd7-b8f2-67b0c855e807
ms.date: 12/05/2018
ms.keywords: CFrameworkQuery interface [Windows Management Instrumentation],GetRequiredProperties method, CFrameworkQuery.GetRequiredProperties, CFrameworkQuery::GetRequiredProperties, GetRequiredProperties, GetRequiredProperties method [Windows Management Instrumentation], GetRequiredProperties method [Windows Management Instrumentation],CFrameworkQuery interface, _hmm_cframeworkquery_getrequiredproperties, frquery/CFrameworkQuery::GetRequiredProperties, wmi.cframeworkquery_getrequiredproperties
req.header: frquery.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CFrameworkQuery::GetRequiredProperties
 - frquery/CFrameworkQuery::GetRequiredProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CFrameworkQuery.GetRequiredProperties
---

# CFrameworkQuery::GetRequiredProperties


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/frquery/nl-frquery-cframeworkquery">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetRequiredProperties</b> method returns a list of all of the properties specified in the <a href="/windows/desktop/WmiSdk/select-statement-for-data-queries">SELECT statement</a> of a query. It returns the properties from both the SELECT and WHERE clauses.

## -parameters

### -param saProperties

Array of properties that were included in the query's <a href="/windows/desktop/WmiSdk/select-statement-for-data-queries">SELECT statement</a>.

## -remarks

If the returned <b>saProperties</b> array is empty, then all properties are required.