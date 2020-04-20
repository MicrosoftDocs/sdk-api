---
UID: NF:frquery.CFrameworkQuery.AllPropertiesAreRequired
title: CFrameworkQuery::AllPropertiesAreRequired (frquery.h)
description: The AllPropertiesAreRequired method indicates whether all of the properties for the instance are requested.helpviewer_keywords: ["AllPropertiesAreRequired","AllPropertiesAreRequired method [Windows Management Instrumentation]","AllPropertiesAreRequired method [Windows Management Instrumentation]","CFrameworkQuery interface","CFrameworkQuery interface [Windows Management Instrumentation]","AllPropertiesAreRequired method","CFrameworkQuery.AllPropertiesAreRequired","CFrameworkQuery::AllPropertiesAreRequired","_hmm_cframeworkquery_allpropertiesarerequired","frquery/CFrameworkQuery::AllPropertiesAreRequired","wmi.cframeworkquery_allpropertiesarerequired"]
old-location: wmi\cframeworkquery_allpropertiesarerequired.htm
tech.root: WmiSdk
ms.assetid: 5c17cae5-c68b-41a3-80ca-88d56be4ab74
ms.date: 12/05/2018
ms.keywords: AllPropertiesAreRequired, AllPropertiesAreRequired method [Windows Management Instrumentation], AllPropertiesAreRequired method [Windows Management Instrumentation],CFrameworkQuery interface, CFrameworkQuery interface [Windows Management Instrumentation],AllPropertiesAreRequired method, CFrameworkQuery.AllPropertiesAreRequired, CFrameworkQuery::AllPropertiesAreRequired, _hmm_cframeworkquery_allpropertiesarerequired, frquery/CFrameworkQuery::AllPropertiesAreRequired, wmi.cframeworkquery_allpropertiesarerequired
f1_keywords:
- frquery/CFrameworkQuery.AllPropertiesAreRequired
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- CFrameworkQuery.AllPropertiesAreRequired
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CFrameworkQuery::AllPropertiesAreRequired


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/frquery/nl-frquery-cframeworkquery">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>AllPropertiesAreRequired</b> method indicates whether all of the properties for the instance are requested.


## -parameters






## -returns



Returns <b>TRUE</b> if all properties are required and <b>FALSE</b> if only a subset of the properties are required.



