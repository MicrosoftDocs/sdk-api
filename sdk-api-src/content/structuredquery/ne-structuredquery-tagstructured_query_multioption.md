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

# tagSTRUCTURED_QUERY_MULTIOPTION enumeration


## -description


A set of flags used by <a href="https://msdn.microsoft.com/3f1d1bed-65b9-4eec-84a0-d77719bc9540">IQueryParser::SetMultiOption</a> to indicate individual options.


## -enum-fields




### -field SQMO_VIRTUAL_PROPERTY

To indicate that a leaf node with property name P and constant C should be replaced with a leaf node with property name Q, operation op, and constant C by <a href="https://msdn.microsoft.com/5eec3f58-745a-4e84-adaa-a88ae3621a6a">IConditionFactory::Resolve</a>, do the following: call <a href="https://msdn.microsoft.com/3f1d1bed-65b9-4eec-84a0-d77719bc9540">IQueryParser::SetMultiOption</a> with SQMO_VIRTUAL_PROPERTY as <i>option</i>, P as <i>pszOptionKey</i>, and for <i>pOptionValue</i> provide a <b>VT_UNKNOWN</b> with an <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface that enumerates exactly two values: a <b>VT_BSTR</b> with value Q, and a <b>VT_I4</b> that is a <a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a> operation.


### -field SQMO_DEFAULT_PROPERTY

To indicate that a leaf node with no property name and a semantic type T (or one that is a subtype of T) should be replaced with one having property name P by <a href="https://msdn.microsoft.com/5eec3f58-745a-4e84-adaa-a88ae3621a6a">IConditionFactory::Resolve</a>, do the following: call <a href="https://msdn.microsoft.com/3f1d1bed-65b9-4eec-84a0-d77719bc9540">IQueryParser::SetMultiOption</a> with SQMO_DEFAULT_PROPERTY  as <i>option</i>, T as <i>pszOptionKey</i>, and for <i>pOptionValue</i> provide a <b>VT_LPWSTR</b> with value P.


### -field SQMO_GENERATOR_FOR_TYPE

To indicate that an <a href="https://msdn.microsoft.com/30fa2fb6-7dfd-41e1-ab4f-5fd80c8a81ec">IConditionGenerator</a> G should be used to recognize named entities of the semantic type named T, and that <a href="https://msdn.microsoft.com/5eec3f58-745a-4e84-adaa-a88ae3621a6a">IConditionFactory::Resolve</a> should generate condition trees for those named entities, call <a href="https://msdn.microsoft.com/3f1d1bed-65b9-4eec-84a0-d77719bc9540">IQueryParser::SetMultiOption</a> with SQMO_GENERATOR_FOR_TYPE as <i>option</i>, T as <i>pszOptionKey</i> and for <i>pOptionValue</i> provide a <b>VT_UNKNOWN</b> with value G.


### -field SQMO_MAP_PROPERTY

Windows 7, and later. To indicate that a node with property P should map to one or more other properties, call <a href="https://msdn.microsoft.com/3f1d1bed-65b9-4eec-84a0-d77719bc9540">IQueryParser::SetMultiOption</a> with SQMO_MAP_PROPERTY as <i>option</i>, P as <i>pszOptionKey</i>, and for <i>pOptionValue</i> provide a <b>VT_VECTOR</b> or <b>VT_LPWSTR</b>, where each string is a property name. During resolustion, this map is added to those of the loaded schema. Calling <b>IQueryParser::SetMultiOption</b> with <i>pOptionValue</i> as <b>VT_NULL</b> removes the mapping.

