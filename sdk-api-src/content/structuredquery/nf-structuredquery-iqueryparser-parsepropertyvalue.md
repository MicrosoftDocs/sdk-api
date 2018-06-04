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

# IQueryParser::ParsePropertyValue


## -description


Parses a condition for a specified property. 


## -parameters




### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Property name.


### -param pszInputString [in]

Type: <b>LPCWSTR</b>

Query string to be parsed, relative to that property.


### -param ppSolution [out, retval]

Type: <b><a href="https://msdn.microsoft.com/a4987e80-7ad9-400d-8c6d-ec3b9a6bf3f1">IQuerySolution</a>**</b>

Receives an <a href="https://msdn.microsoft.com/a4987e80-7ad9-400d-8c6d-ec3b9a6bf3f1">IQuerySolution</a> object. The calling application must release it by calling its <a href="_com_IUnknown_Release">IUnknown::Release</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            The input string can be anything that could have been written immediately after a property in a structured query. For example, "from:(bill OR alex)" would be a valid structured query, so passing System.StructuredQuery.Virtual.From (for which From is a keyword) in the <i>pszPropertyName</i> parameter and "(bill OR alex)" or "bill OR alex" in the <i>pszInputString</i> parameter would be valid. This would result in an <b>OR</b> of leaf nodes that relate the System.StructuredQuery.Virtual.From property with the strings "bill" and "alex".
            



