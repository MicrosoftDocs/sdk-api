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

# ICondition::GetInputTerms


## -description


For a leaf node, <b>ICondition::GetInputTerms</b> retrieves information about what parts (or ranges) of the input string produced the property, the operation, and the value for the search condition node.


## -parameters




### -param ppPropertyTerm [out, optional]

Type: <b><a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> interface that provides information about what part of the input string produced the property of the leaf node, if that can be determined; otherwise, this parameter is set to <b>NULL</b>.


### -param ppOperationTerm [out, optional]

Type: <b><a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> interface that provides information about what part of the input string produced the operation of the leaf node, if that can be determined; otherwise, this parameter is set to <b>NULL</b>.


### -param ppValueTerm [out, optional]

Type: <b><a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> interface that provides information about what part of the input string produced the value of the leaf node, if that can be determined; otherwise, this parameter is set to <b>NULL</b>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Any or all of the parameters <i>ppPropertyTerm</i>, <i>ppOperationTerm</i> and <i>ppValueTerm</i> can be <b>NULL</b>.

Each <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> object retrieved by this method represents a range of tokens from the input string. The range tokens identifies the substring that produced the property, operation, or value of the input string. The <b>IRichChunk</b>'s <a href="_stg_propvariant">PROPVARIANT</a> out parameter is not used.




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<b>Reference</b>
 

 

