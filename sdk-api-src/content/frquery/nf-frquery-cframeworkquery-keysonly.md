---
UID: NF:frquery.CFrameworkQuery.KeysOnly
title: CFrameworkQuery::KeysOnly (frquery.h)
description: The KeysOnly method indicates whether only the key properties are required.
helpviewer_keywords: ["CFrameworkQuery interface [Windows Management Instrumentation]","KeysOnly method","CFrameworkQuery.KeysOnly","CFrameworkQuery::KeysOnly","KeysOnly","KeysOnly method [Windows Management Instrumentation]","KeysOnly method [Windows Management Instrumentation]","CFrameworkQuery interface","_hmm_cframeworkquery_keysonly","frquery/CFrameworkQuery::KeysOnly","wmi.cframeworkquery_keysonly"]
old-location: wmi\cframeworkquery_keysonly.htm
tech.root: wmi
ms.assetid: 977030f8-264f-4fa2-8941-e419cd28c569
ms.date: 12/05/2018
ms.keywords: CFrameworkQuery interface [Windows Management Instrumentation],KeysOnly method, CFrameworkQuery.KeysOnly, CFrameworkQuery::KeysOnly, KeysOnly, KeysOnly method [Windows Management Instrumentation], KeysOnly method [Windows Management Instrumentation],CFrameworkQuery interface, _hmm_cframeworkquery_keysonly, frquery/CFrameworkQuery::KeysOnly, wmi.cframeworkquery_keysonly
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
 - CFrameworkQuery::KeysOnly
 - frquery/CFrameworkQuery::KeysOnly
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
 - CFrameworkQuery.KeysOnly
---

# CFrameworkQuery::KeysOnly


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/frquery/nl-frquery-cframeworkquery">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>KeysOnly</b> method indicates whether only the key properties are required.



## -returns

Returns <b>TRUE</b> if only the key properties are required and <b>FALSE</b> if non-key properties are required.
