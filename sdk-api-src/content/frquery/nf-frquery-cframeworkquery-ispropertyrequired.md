---
UID: NF:frquery.CFrameworkQuery.IsPropertyRequired
title: CFrameworkQuery::IsPropertyRequired (frquery.h)
description: The IsPropertyRequired method determines if a particular property was requested by the query. Both the SELECT and WHERE clauses are checked.
helpviewer_keywords: ["CFrameworkQuery interface [Windows Management Instrumentation]","IsPropertyRequired method","CFrameworkQuery.IsPropertyRequired","CFrameworkQuery::IsPropertyRequired","IsPropertyRequired","IsPropertyRequired method [Windows Management Instrumentation]","IsPropertyRequired method [Windows Management Instrumentation]","CFrameworkQuery interface","_hmm_cframeworkquery_ispropertyrequired","frquery/CFrameworkQuery::IsPropertyRequired","wmi.cframeworkquery_ispropertyrequired"]
old-location: wmi\cframeworkquery_ispropertyrequired.htm
tech.root: wmi
ms.assetid: 36f5a261-435c-494d-aae5-a420eee030f2
ms.date: 12/05/2018
ms.keywords: CFrameworkQuery interface [Windows Management Instrumentation],IsPropertyRequired method, CFrameworkQuery.IsPropertyRequired, CFrameworkQuery::IsPropertyRequired, IsPropertyRequired, IsPropertyRequired method [Windows Management Instrumentation], IsPropertyRequired method [Windows Management Instrumentation],CFrameworkQuery interface, _hmm_cframeworkquery_ispropertyrequired, frquery/CFrameworkQuery::IsPropertyRequired, wmi.cframeworkquery_ispropertyrequired
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
 - CFrameworkQuery::IsPropertyRequired
 - frquery/CFrameworkQuery::IsPropertyRequired
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
 - CFrameworkQuery.IsPropertyRequired
---

# CFrameworkQuery::IsPropertyRequired


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/frquery/nl-frquery-cframeworkquery">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>IsPropertyRequired</b> method determines if a particular property was requested by the query. Both the <b>SELECT</b> and <b>WHERE</b> clauses are checked.

## -parameters

### -param propName

Name of property that is checked.

## -returns

Returns <b>TRUE</b> if the property specified by <i>propName</i> was requested and <b>FALSE</b> if it was not requested.