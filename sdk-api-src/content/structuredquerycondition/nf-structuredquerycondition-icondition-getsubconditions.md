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

# ICondition::GetSubConditions


## -description



            Retrieves a collection of the subconditions of the search condition node and the IID of the interface for enumerating the collection.
        


## -parameters




### -param riid [in]

Type: <b>REFIID</b>


                The desired IID of the enumerating interface: either IID_IEnumUnknown, IID_IEnumVARIANT or (for a negation condition) IID_ICondition.
            


### -param ppv [out, retval]

Type: <b>void**</b>


                Receives a collection of zero or more <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> objects. Each object is a subcondition of this condition node. If <i>riid</i> was IID_ICondition and this is a negation condition, this parameter receives the single subcondition.
            


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is a leaf node, or an error value otherwise.




## -remarks



The <i>riid</i> parameter must be the <b>GUID</b> of an <a href="_com_IEnumUnknown">IEnumUnknown</a> or <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface or in the case of a negation node, IID_ICondition.

If the subcondition is a negation node, <i>ppv</i> is set to an enumeration of one element.

If the node is a conjunction or disjunction node, <i>ppv</i> is set to an enumeration of the subconditions.




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<b>Reference</b>
 

 

