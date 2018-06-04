---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tag_SWbemAssocQueryInf structure


## -description


The <b>SWbemAssocQueryInf</b> structure contains information from the <a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">IWbemQuery::GetAnalysis</a> method when you use the <b>WMIQ_ANALYSIS_ASSOC_QUERY</b> analysis type.


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

Pointer to an <a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a> object.


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




<a href="https://msdn.microsoft.com/4a0c0c1d-3d84-491f-8379-d164821fa71b">IWbemQuery</a>



<a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">IWbemQuery::GetAnalysis</a>
 

 

