---
UID: NE:wmiutils.__MIDL___MIDL_itf_wmiutils_0000_0001_0001
title: "__MIDL___MIDL_itf_wmiutils_0000_0001_0001"
author: windows-sdk-content
description: Contains constants used to specify the type of analysis to perform by using the GetAnalysis method.
old-location: wmi\wmiq_analysis_type.htm
old-project: WmiSdk
ms.assetid: 427f5ca7-4172-4bd0-9469-5b2ad1cb4c53
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: WMIQ_ANALYSIS_ASSOC_QUERY, WMIQ_ANALYSIS_PROP_ANALYSIS_MATRIX, WMIQ_ANALYSIS_QUERY_TEXT, WMIQ_ANALYSIS_RESERVED, WMIQ_ANALYSIS_RPN_SEQUENCE, WMIQ_ANALYSIS_TYPE, WMIQ_ANALYSIS_TYPE enumeration [Windows Management Instrumentation], __MIDL___MIDL_itf_wmiutils_0000_0001_0001, wmi.wmiq_analysis_type, wmiutils/WMIQ_ANALYSIS_ASSOC_QUERY, wmiutils/WMIQ_ANALYSIS_PROP_ANALYSIS_MATRIX, wmiutils/WMIQ_ANALYSIS_QUERY_TEXT, wmiutils/WMIQ_ANALYSIS_RESERVED, wmiutils/WMIQ_ANALYSIS_RPN_SEQUENCE, wmiutils/WMIQ_ANALYSIS_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: WMIQ_ANALYSIS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WMIUtils.h
api_name:
-	WMIQ_ANALYSIS_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# __MIDL___MIDL_itf_wmiutils_0000_0001_0001 enumeration


## -description


Contains constants used to specify the type of analysis to perform by using the <a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">GetAnalysis</a> method.


## -enum-fields




### -field WMIQ_ANALYSIS_RPN_SEQUENCE

Used if the query has a SELECT clause. When this type of analysis is used,  <i>pAnalysis</i> points to an <a href="https://msdn.microsoft.com/0f7e77a8-4ee6-421b-be4a-b58055a58c39">SWbemRpnEncodedQuery</a> structure.


### -field WMIQ_ANALYSIS_ASSOC_QUERY

Used to return information about association type queries. When this type of analysis is used,  <i>pAnalysis</i> points to an <a href="https://msdn.microsoft.com/8312b324-a698-4957-bd76-3129398e4886">SWbemAssocQueryInf</a> structure.


### -field WMIQ_ANALYSIS_PROP_ANALYSIS_MATRIX

Unused.  Reserved for future use.


### -field WMIQ_ANALYSIS_QUERY_TEXT

Used to return a text string that has the original query text. If this type of analysis is used,  <i>pAnalysis</i> points to a text string that contains the original query text.

You can use this parameter if  a parser object is passed to another method.


### -field WMIQ_ANALYSIS_RESERVED

Unused.  Reserved for future use.

