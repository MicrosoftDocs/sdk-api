---
UID: NF:wmiutils.IWbemQuery.Parse
title: IWbemQuery::Parse
author: windows-sdk-content
description: Parses a query string.
old-location: wmi\iwbemquery_parse.htm
old-project: WmiSdk
ms.assetid: 372b004f-322e-459c-8db0-150b0483aa34
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IWbemQuery class [Windows Management Instrumentation],Parse method, IWbemQuery.Parse, IWbemQuery::Parse, Parse, Parse method [Windows Management Instrumentation], Parse method [Windows Management Instrumentation],IWbemQuery class, _hmm_iwbemquery_parse, wmi.iwbemquery_parse, wmiutils/IWbemQuery::Parse
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmiutils.h
req.include-header: 
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
req.typenames: WMIQ_ASSOCQ_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemQuery.Parse
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemQuery::Parse


## -description


The 
<b>IWbemQuery::Parse</b> method parses a query string.


## -parameters




### -param pszLang [in]

Language of the query. Must be either "WQL" or "SQL" (case-sensitive). Any other value will result in the method failing and <b>WBEM_E_INVALID_PARAMETER</b> being returned.


### -param pszQuery [in]

Valid WQL or SQL WMI query.


### -param uFlags [in]

Reserved for future use. Must be 0 (zero).


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/4a0c0c1d-3d84-491f-8379-d164821fa71b">IWbemQuery</a>
 

 

