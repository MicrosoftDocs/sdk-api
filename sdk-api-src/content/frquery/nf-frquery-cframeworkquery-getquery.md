---
UID: NF:frquery.CFrameworkQuery.GetQuery
title: CFrameworkQuery::GetQuery (frquery.h)
description: The GetQuery method retrieves the actual WQL command associated with the CFrameworkQuery object.
helpviewer_keywords: ["?GetQuery@CFrameworkQuery@@QAEABVCHString@@XZ","CFrameworkQuery interface [Windows Management Instrumentation]","GetQuery method","CFrameworkQuery.GetQuery","CFrameworkQuery::GetQuery","GetQuery","GetQuery method [Windows Management Instrumentation]","GetQuery method [Windows Management Instrumentation]","CFrameworkQuery interface","_hmm_cframeworkquery_getquery","frquery/CFrameworkQuery::GetQuery","wmi.cframeworkquery_getquery"]
old-location: wmi\cframeworkquery_getquery.htm
tech.root: wmi
ms.assetid: 2f7b5057-8522-4ef3-bf5a-3b96b72128b3
ms.date: 12/05/2018
ms.keywords: ?GetQuery@CFrameworkQuery@@QAEABVCHString@@XZ, CFrameworkQuery interface [Windows Management Instrumentation],GetQuery method, CFrameworkQuery.GetQuery, CFrameworkQuery::GetQuery, GetQuery, GetQuery method [Windows Management Instrumentation], GetQuery method [Windows Management Instrumentation],CFrameworkQuery interface, _hmm_cframeworkquery_getquery, frquery/CFrameworkQuery::GetQuery, wmi.cframeworkquery_getquery
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
 - CFrameworkQuery::GetQuery
 - frquery/CFrameworkQuery::GetQuery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CFrameworkQuery.GetQuery
 - ?GetQuery@CFrameworkQuery@@QAEABVCHString@@XZ
---

# CFrameworkQuery::GetQuery


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/frquery/nl-frquery-cframeworkquery">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetQuery</b> method retrieves the actual WQL command associated with the <a href="/windows/desktop/api/frquery/nl-frquery-cframeworkquery">CFrameworkQuery</a> object.



## -returns

Returns the WQL command if the operation was successful and <b>NULL</b> otherwise.

## -remarks

If <b>GetQuery</b> is called within <a href="/windows/desktop/api/provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)">Provider::GetObject</a>, the WQL command line does not contain a <a href="/windows/desktop/WmiSdk/select-statement-for-data-queries">WHERE</a> clause.
