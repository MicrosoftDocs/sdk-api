---
UID: NF:frquery.CFrameworkQuery.GetRequiredProperties
title: CFrameworkQuery::GetRequiredProperties
author: windows-sdk-content
description: The GetRequiredProperties method returns a list of all of the properties specified in the SELECT statement of a query. It returns the properties from both the SELECT and WHERE clauses.
old-location: wmi\cframeworkquery_getrequiredproperties.htm
old-project: WmiSdk
ms.assetid: cf02aa01-6d56-4fd7-b8f2-67b0c855e807
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CFrameworkQuery interface [Windows Management Instrumentation],GetRequiredProperties method, CFrameworkQuery.GetRequiredProperties, CFrameworkQuery::GetRequiredProperties, GetRequiredProperties, GetRequiredProperties method [Windows Management Instrumentation], GetRequiredProperties method [Windows Management Instrumentation],CFrameworkQuery interface, _hmm_cframeworkquery_getrequiredproperties, frquery/CFrameworkQuery::GetRequiredProperties, wmi.cframeworkquery_getrequiredproperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: frquery.h
req.include-header: FwCommon.h
req.redist: 
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
 - CFrameworkQuery.GetRequiredProperties
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Internet Explorer 5
---

# CFrameworkQuery::GetRequiredProperties


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/60a7d83c-cfea-41fa-8d97-321127d33c43">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetRequiredProperties</b> method returns a list of all of the properties specified in the <a href="https://msdn.microsoft.com/9c1a164e-4728-4fbe-8a49-b571005a46ec">SELECT statement</a> of a query. It returns the properties from both the SELECT and WHERE clauses.


## -parameters




### -param saProperties

Array of properties that were included in the query's <a href="https://msdn.microsoft.com/9c1a164e-4728-4fbe-8a49-b571005a46ec">SELECT statement</a>.


## -returns



This method has no return values.




## -remarks



If the returned <b>saProperties</b> array is empty, then all properties are required.



