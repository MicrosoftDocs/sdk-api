---
UID: NS:wmiutils.tag_SWbemAssocQueryInf
title: SWbemAssocQueryInf (wmiutils.h)
description: Contains information from the IWbemQuery::GetAnalysis method when you use the WMIQ_ANALYSIS_ASSOC_QUERY analysis type.
helpviewer_keywords: ["SWbemAssocQueryInf","SWbemAssocQueryInf structure [Windows Management Instrumentation]","WMIQ_ASSOCQ_ASSOCCLASS","WMIQ_ASSOCQ_ASSOCIATORS","WMIQ_ASSOCQ_CLASSDEFONLY","WMIQ_ASSOCQ_CLASSREFSONLY","WMIQ_ASSOCQ_KEYSONLY","WMIQ_ASSOCQ_REFERENCES","WMIQ_ASSOCQ_REQUIREDASSOCQUALIFIER","WMIQ_ASSOCQ_REQUIREDQUALIFIER","WMIQ_ASSOCQ_RESULTCLASS","WMIQ_ASSOCQ_RESULTROLE","WMIQ_ASSOCQ_ROLE","WMIQ_ASSOCQ_SCHEMAONLY","wmi.swbemassocqueryinf","wmiutils/SWbemAssocQueryInf"]
old-location: wmi\swbemassocqueryinf.htm
tech.root: wmi
ms.assetid: 8312b324-a698-4957-bd76-3129398e4886
ms.date: 12/05/2018
ms.keywords: SWbemAssocQueryInf, SWbemAssocQueryInf structure [Windows Management Instrumentation], WMIQ_ASSOCQ_ASSOCCLASS, WMIQ_ASSOCQ_ASSOCIATORS, WMIQ_ASSOCQ_CLASSDEFONLY, WMIQ_ASSOCQ_CLASSREFSONLY, WMIQ_ASSOCQ_KEYSONLY, WMIQ_ASSOCQ_REFERENCES, WMIQ_ASSOCQ_REQUIREDASSOCQUALIFIER, WMIQ_ASSOCQ_REQUIREDQUALIFIER, WMIQ_ASSOCQ_RESULTCLASS, WMIQ_ASSOCQ_RESULTROLE, WMIQ_ASSOCQ_ROLE, WMIQ_ASSOCQ_SCHEMAONLY, wmi.swbemassocqueryinf, wmiutils/SWbemAssocQueryInf
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
req.typenames: SWbemAssocQueryInf
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_SWbemAssocQueryInf
 - wmiutils/tag_SWbemAssocQueryInf
 - SWbemAssocQueryInf
 - wmiutils/SWbemAssocQueryInf
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
 - SWbemAssocQueryInf
---

# SWbemAssocQueryInf structure


## -description

The <b>SWbemAssocQueryInf</b> structure contains information from the <a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">IWbemQuery::GetAnalysis</a> method when you use the <b>WMIQ_ANALYSIS_ASSOC_QUERY</b> analysis type.

## -struct-fields

### -field m_uVersion

Value must be 2.

### -field m_uAnalysisType

Value must be 2.

### -field m_uFeatureMask

Bit values that indicate the features in a query.



#### WMIQ_ASSOCQ_ASSOCIATORS (1 (0x1))

Associators exist in the query.



#### WMIQ_ASSOCQ_REFERENCES (2 (0x2))

References exist in the query.



#### WMIQ_ASSOCQ_RESULTCLASS (4 (0x4))

A result class is specified in the query.



#### WMIQ_ASSOCQ_ASSOCCLASS (8 (0x8))

An association class is specified in the query.



#### WMIQ_ASSOCQ_ROLE (16 (0x10))

A role is specified in the query.



#### WMIQ_ASSOCQ_RESULTROLE (32 (0x20))

A result role is specified in the query.



#### WMIQ_ASSOCQ_REQUIREDQUALIFIER (64 (0x40))

Required qualifiers are specified in the query.



#### WMIQ_ASSOCQ_REQUIREDASSOCQUALIFIER (128 (0x80))

Required association qualifiers are specified in the query.



#### WMIQ_ASSOCQ_CLASSDEFONLY (256 (0x100))

The query specifies class definitions only.



#### WMIQ_ASSOCQ_KEYSONLY (512 (0x200))

The query contains the <b>KEYSONLY</b> keyword.



#### WMIQ_ASSOCQ_SCHEMAONLY (1024 (0x400))

The query returns only the schema.



#### WMIQ_ASSOCQ_CLASSREFSONLY (2048 (0x800))

The query returns only the class references.

### -field m_pPath

Pointer to an <a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a> object.

### -field m_pszPath

String representation of the object path used in the query.

### -field m_pszQueryText

Text of the original query.

### -field m_pszResultClass

String representation of the result class. If there is no result class, this field is <b>NULL</b>.

### -field m_pszAssocClass

String representation of the association class. If there is no result class, this field is <b>NULL</b>.

### -field m_pszRole

String representation of the role. If there is no role, this field is <b>NULL</b>.

### -field m_pszResultRole

String representation of the result role. If there is no result role, this field is <b>NULL</b>.

### -field m_pszRequiredQualifier

String representation of the required qualifier. If no qualifiers are required, this field is <b>NULL</b>.

### -field m_pszRequiredAssocQualifier

Pointer to a list of required association qualifiers.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbemquery">IWbemQuery</a>



<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">IWbemQuery::GetAnalysis</a>