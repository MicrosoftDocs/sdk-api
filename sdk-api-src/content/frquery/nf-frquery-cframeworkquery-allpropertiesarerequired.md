---
UID: NF:frquery.CFrameworkQuery.AllPropertiesAreRequired
title: CFrameworkQuery::AllPropertiesAreRequired method
author: windows-driver-content
description: The AllPropertiesAreRequired method indicates whether all of the properties for the instance are requested.
old-location: wmi\cframeworkquery_allpropertiesarerequired.htm
old-project: WmiSdk
ms.assetid: 5c17cae5-c68b-41a3-80ca-88d56be4ab74
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: AllPropertiesAreRequired method [Windows Management Instrumentation], AllPropertiesAreRequired method [Windows Management Instrumentation], CFrameworkQuery interface, AllPropertiesAreRequired,CFrameworkQuery.AllPropertiesAreRequired, CFrameworkQuery, CFrameworkQuery interface [Windows Management Instrumentation], AllPropertiesAreRequired method, CFrameworkQuery::AllPropertiesAreRequired, _hmm_cframeworkquery_allpropertiesarerequired, frquery/CFrameworkQuery::AllPropertiesAreRequired, wmi.cframeworkquery_allpropertiesarerequired
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CFrameworkQuery.AllPropertiesAreRequired
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Internet Explorer 5
---

# CFrameworkQuery::AllPropertiesAreRequired method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/60a7d83c-cfea-41fa-8d97-321127d33c43">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>AllPropertiesAreRequired</b> method indicates whether all of the properties for the instance are requested.


## -parameters






## -returns



Returns <b>TRUE</b> if all properties are required and <b>FALSE</b> if only a subset of the properties are required.



