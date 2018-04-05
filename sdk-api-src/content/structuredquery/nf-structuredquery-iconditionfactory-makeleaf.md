---
UID: NF:structuredquery.IConditionFactory.MakeLeaf
title: IConditionFactory::MakeLeaf method
author: windows-driver-content
description: Creates a leaf condition node that represents a comparison of property value and constant value.
old-location: search\_search_IConditionFactory_MakeLeaf.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\makeleaf.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IConditionFactory, IConditionFactory interface [search], MakeLeaf method, IConditionFactory::MakeLeaf, MakeLeaf method [search], MakeLeaf method [search], IConditionFactory interface, MakeLeaf,IConditionFactory.MakeLeaf, _search_IConditionFactory_MakeLeaf, search._search_IConditionFactory_MakeLeaf, structuredquery/IConditionFactory::MakeLeaf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IConditionFactory.MakeLeaf
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IConditionFactory::MakeLeaf method


## -description



          Creates a leaf condition node that represents a comparison of property value and constant value.
        


## -parameters




### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>


              The name of a property to be compared, or <b>NULL</b> for an unspecified property. The locale name of the leaf node is LOCALE_NAME_USER_DEFAULT.


### -param cop [in]

Type: <b><a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a></b>


              A <a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a> enumeration.
            


### -param pszValueType [in]

Type: <b>LPCWSTR</b>


              The name of a semantic type of the value, or <b>NULL</b> for a plain string.
            


### -param ppropvar [in]

Type: <b>PROPVARIANT const*</b>


                  The constant value against which the property value should be compared.
            


### -param pPropertyNameTerm [in]

Type: <b><a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a>*</b>


              A pointer to an <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> that identifies the range of the input string that repesents the property. It can be <b>NULL</b>.
            


### -param pOperationTerm [in]

Type: <b><a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a>*</b>


              A pointer to an <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> that identifies the range of the input string that repesents the operation. It can be <b>NULL</b>.
            


### -param pValueTerm [in]

Type: <b><a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a>*</b>


              A pointer to an <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> that identifies the range of the input string that repesents the value. It can be <b>NULL</b>.
            


### -param fExpand [in]

Type: <b>BOOL</b>


              If <b>TRUE</b> and <i>pszPropertyName</i> identifies a virtual property, the resulting node is not a leaf node; instead, it is a disjunction of leaf condition nodes, each of which corresponds to one expansion of the virtual property.
            


### -param ppcResult [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>**</b>


              Receives a pointer to the new <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> leaf node.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For more information about leaf node terms (property, value, and operation), see 
<a href="https://msdn.microsoft.com/9d169fb4-177f-42e6-a24c-bb0052d1d62b">ICondition::GetInputTerms</a>.

A virtual property has one or more metadata items in which the key is "MapsToRelation" and the value is a property name (which is one expansion of the property). For more information about metadata, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn915567">MetaData</a>. 
     




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<a href="https://msdn.microsoft.com/5ac0acb1-67f0-43f0-b1c1-2d8cf682a277">IConditionFactory2</a>



<b>Reference</b>
 

 

