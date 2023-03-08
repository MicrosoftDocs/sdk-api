---
UID: NE:wmiutils.__MIDL___MIDL_itf_wmiutils_0000_0001_0001
title: WMIQ_ANALYSIS_TYPE (wmiutils.h)
description: Contains constants used to specify the type of analysis to perform by using the GetAnalysis method.
helpviewer_keywords: ["WMIQ_ANALYSIS_ASSOC_QUERY","WMIQ_ANALYSIS_PROP_ANALYSIS_MATRIX","WMIQ_ANALYSIS_QUERY_TEXT","WMIQ_ANALYSIS_RESERVED","WMIQ_ANALYSIS_RPN_SEQUENCE","WMIQ_ANALYSIS_TYPE","WMIQ_ANALYSIS_TYPE enumeration [Windows Management Instrumentation]","wmi.wmiq_analysis_type","wmiutils/WMIQ_ANALYSIS_ASSOC_QUERY","wmiutils/WMIQ_ANALYSIS_PROP_ANALYSIS_MATRIX","wmiutils/WMIQ_ANALYSIS_QUERY_TEXT","wmiutils/WMIQ_ANALYSIS_RESERVED","wmiutils/WMIQ_ANALYSIS_RPN_SEQUENCE","wmiutils/WMIQ_ANALYSIS_TYPE"]
old-location: wmi\wmiq_analysis_type.htm
tech.root: wmi
ms.assetid: 427f5ca7-4172-4bd0-9469-5b2ad1cb4c53
ms.date: 12/05/2018
ms.keywords: WMIQ_ANALYSIS_ASSOC_QUERY, WMIQ_ANALYSIS_PROP_ANALYSIS_MATRIX, WMIQ_ANALYSIS_QUERY_TEXT, WMIQ_ANALYSIS_RESERVED, WMIQ_ANALYSIS_RPN_SEQUENCE, WMIQ_ANALYSIS_TYPE, WMIQ_ANALYSIS_TYPE enumeration [Windows Management Instrumentation], wmi.wmiq_analysis_type, wmiutils/WMIQ_ANALYSIS_ASSOC_QUERY, wmiutils/WMIQ_ANALYSIS_PROP_ANALYSIS_MATRIX, wmiutils/WMIQ_ANALYSIS_QUERY_TEXT, wmiutils/WMIQ_ANALYSIS_RESERVED, wmiutils/WMIQ_ANALYSIS_RPN_SEQUENCE, wmiutils/WMIQ_ANALYSIS_TYPE
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WMIQ_ANALYSIS_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wmiutils_0000_0001_0001
 - wmiutils/__MIDL___MIDL_itf_wmiutils_0000_0001_0001
 - WMIQ_ANALYSIS_TYPE
 - wmiutils/WMIQ_ANALYSIS_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WMIUtils.h
api_name:
 - WMIQ_ANALYSIS_TYPE
---

# WMIQ_ANALYSIS_TYPE enumeration


## -description

Contains constants used to specify the type of analysis to perform by using the <a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">GetAnalysis</a> method.

## -enum-fields

### -field WMIQ_ANALYSIS_RPN_SEQUENCE:0x1

Used if the query has a SELECT clause. When this type of analysis is used,  <i>pAnalysis</i> points to an <a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemrpnencodedquery">SWbemRpnEncodedQuery</a> structure.

### -field WMIQ_ANALYSIS_ASSOC_QUERY:0x2

Used to return information about association type queries. When this type of analysis is used,  <i>pAnalysis</i> points to an <a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemassocqueryinf">SWbemAssocQueryInf</a> structure.

### -field WMIQ_ANALYSIS_PROP_ANALYSIS_MATRIX:0x3

Unused.  Reserved for future use.

### -field WMIQ_ANALYSIS_QUERY_TEXT:0x4

Used to return a text string that has the original query text. If this type of analysis is used,  <i>pAnalysis</i> points to a text string that contains the original query text.

You can use this parameter if  a parser object is passed to another method.

### -field WMIQ_ANALYSIS_RESERVED:0x8000000

Unused.  Reserved for future use.
