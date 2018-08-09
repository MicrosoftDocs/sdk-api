---
UID: NF:frquery.CFrameworkQuery.IsPropertyRequired
title: CFrameworkQuery::IsPropertyRequired
author: windows-sdk-content
description: The IsPropertyRequired method determines if a particular property was requested by the query. Both the SELECT and WHERE clauses are checked.
old-location: wmi\cframeworkquery_ispropertyrequired.htm
old-project: WmiSdk
ms.assetid: 36f5a261-435c-494d-aae5-a420eee030f2
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CFrameworkQuery interface [Windows Management Instrumentation],IsPropertyRequired method, CFrameworkQuery.IsPropertyRequired, CFrameworkQuery::IsPropertyRequired, IsPropertyRequired, IsPropertyRequired method [Windows Management Instrumentation], IsPropertyRequired method [Windows Management Instrumentation],CFrameworkQuery interface, _hmm_cframeworkquery_ispropertyrequired, frquery/CFrameworkQuery::IsPropertyRequired, wmi.cframeworkquery_ispropertyrequired
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
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
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Internet Explorer 5
---

# CFrameworkQuery::IsPropertyRequired


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/60a7d83c-cfea-41fa-8d97-321127d33c43">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>IsPropertyRequired</b> method determines if a particular property was requested by the query. Both the <b>SELECT</b> and <b>WHERE</b> clauses are checked.


## -parameters




### -param propName

Name of property that is checked.


## -returns



Returns <b>TRUE</b> if the property specified by <i>propName</i> was requested and <b>FALSE</b> if it was not requested.



