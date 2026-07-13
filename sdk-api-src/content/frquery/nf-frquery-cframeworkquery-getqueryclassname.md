---
UID: NF:frquery.CFrameworkQuery.GetQueryClassName
title: CFrameworkQuery::GetQueryClassName (frquery.h)
description: The GetQueryClassName method retrieves the class name from the query.
helpviewer_keywords: ["CFrameworkQuery interface [Windows Management Instrumentation]","GetQueryClassName method","CFrameworkQuery.GetQueryClassName","CFrameworkQuery::GetQueryClassName","GetQueryClassName","GetQueryClassName method [Windows Management Instrumentation]","GetQueryClassName method [Windows Management Instrumentation]","CFrameworkQuery interface","_hmm_cframeworkquery_getqueryclassname","frquery/CFrameworkQuery::GetQueryClassName","wmi.cframeworkquery_getqueryclassname"]
old-location: wmi\cframeworkquery_getqueryclassname.htm
tech.root: wmi
ms.assetid: 6cb3da43-dab1-4049-9793-d62f027efe1c
ms.date: 12/05/2018
ms.keywords: CFrameworkQuery interface [Windows Management Instrumentation],GetQueryClassName method, CFrameworkQuery.GetQueryClassName, CFrameworkQuery::GetQueryClassName, GetQueryClassName, GetQueryClassName method [Windows Management Instrumentation], GetQueryClassName method [Windows Management Instrumentation],CFrameworkQuery interface, _hmm_cframeworkquery_getqueryclassname, frquery/CFrameworkQuery::GetQueryClassName, wmi.cframeworkquery_getqueryclassname
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
 - CFrameworkQuery::GetQueryClassName
 - frquery/CFrameworkQuery::GetQueryClassName
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
 - CFrameworkQuery.GetQueryClassName
---

# CFrameworkQuery::GetQueryClassName


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/frquery/nl-frquery-cframeworkquery">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetQueryClassName</b> method retrieves the class name from the query.



## -returns

Returns the class name if the operation was successful and <b>NULL</b> otherwise.

## -remarks

It is the developer's responsibility to call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> on the <b>BSTR</b> returned by this method to avoid a memory leak.
