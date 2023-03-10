---
UID: NS:wmiutils.tag_SWbemQueryQualifiedName
title: SWbemQueryQualifiedName (wmiutils.h)
description: The SWbemQueryQualifiedName structure stores property names for the IWbemQuery::GetAnalysis method.
helpviewer_keywords: ["SWbemQueryQualifiedName","SWbemQueryQualifiedName structure [Windows Management Instrumentation]","wmi.swbemqueryqualifiedname","wmiutils/SWbemQueryQualifiedName"]
old-location: wmi\swbemqueryqualifiedname.htm
tech.root: wmi
ms.assetid: ce8031a1-b30f-4ff6-90d8-42e46e1b6d89
ms.date: 12/05/2018
ms.keywords: SWbemQueryQualifiedName, SWbemQueryQualifiedName structure [Windows Management Instrumentation], wmi.swbemqueryqualifiedname, wmiutils/SWbemQueryQualifiedName
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
req.typenames: SWbemQueryQualifiedName
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_SWbemQueryQualifiedName
 - wmiutils/tag_SWbemQueryQualifiedName
 - SWbemQueryQualifiedName
 - wmiutils/SWbemQueryQualifiedName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmiutils.h
api_name:
 - SWbemQueryQualifiedName
---

# SWbemQueryQualifiedName structure


## -description

The <b>SWbemQueryQualifiedName</b> structure stores property names for the <a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">IWbemQuery::GetAnalysis</a> method.

## -struct-fields

### -field m_uVersion

Unused. Always 1 (one).

### -field m_uTokenType

Unused. Always 1 (one).

### -field m_uNameListSize

Number of elements in the list of names. For example, for the  "propName" property,  <b>m_uNameListSize</b> is 1 (one) and <b>m_ppszNameList</b> is "propName".

### -field m_ppszNameList

List of property names. For example, for the  "propName" property, <b>m_uNameListSize</b> is 1 (one) and <b>m_ppszNameList</b> is "propName".

### -field m_bArraysUsed

Unused. Always <b>false</b>.

### -field m_pbArrayElUsed

Unused. Always <b>NULL</b>.

### -field m_puArrayIndex

Unused. Always <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbemquery">IWbemQuery</a>



<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">IWbemQuery::GetAnalysis</a>



<a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemrpnencodedquery">SWbemRpnEncodedQuery</a>