---
UID: NF:frquery.CFrameworkQuery.GetQuery
title: CFrameworkQuery::GetQuery
author: windows-sdk-content
description: The GetQuery method retrieves the actual WQL command associated with the CFrameworkQuery object.
old-location: wmi\cframeworkquery_getquery.htm
old-project: WmiSdk
ms.assetid: 2f7b5057-8522-4ef3-bf5a-3b96b72128b3
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "?GetQuery@CFrameworkQuery@@QAEABVCHString@@XZ, CFrameworkQuery interface [Windows Management Instrumentation],GetQuery method, CFrameworkQuery.GetQuery, CFrameworkQuery::GetQuery, GetQuery, GetQuery method [Windows Management Instrumentation], GetQuery method [Windows Management Instrumentation],CFrameworkQuery interface, _hmm_cframeworkquery_getquery, frquery/CFrameworkQuery::GetQuery, wmi.cframeworkquery_getquery"
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
 - CFrameworkQuery.GetQuery
 - ?GetQuery@CFrameworkQuery@@QAEABVCHString@@XZ
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Internet Explorer 5
---

# CFrameworkQuery::GetQuery


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/60a7d83c-cfea-41fa-8d97-321127d33c43">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetQuery</b> method retrieves the actual WQL command associated with the <a href="https://msdn.microsoft.com/60a7d83c-cfea-41fa-8d97-321127d33c43">CFrameworkQuery</a> object.


## -parameters






## -returns



Returns the WQL command if the operation was successful and <b>NULL</b> otherwise.




## -remarks



If <b>GetQuery</b> is called within <a href="https://msdn.microsoft.com/c8e2633a-cbea-422c-9598-1b1b1104bbc2">Provider::GetObject</a>, the WQL command line does not contain a <a href="https://msdn.microsoft.com/9c1a164e-4728-4fbe-8a49-b571005a46ec">WHERE</a> clause.



