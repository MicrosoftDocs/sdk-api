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

# IQuerySolution::GetLexicalData


## -description



          Reports the query string, how it was tokenized, and what language code identifier (LCID) and word breaker were used to parse it.
        


## -parameters




### -param ppszInputString [out]

Type: <b>LPWSTR*</b>


              Receives the query string. This parameter can be <b>NULL</b>.
            


### -param ppTokens [out]

Type: <b><a href="https://msdn.microsoft.com/e7f5b3ce-dae2-41ec-90ff-9ab49e0301bd">ITokenCollection</a>**</b>


              Receives a pointer to an <a href="https://msdn.microsoft.com/e7f5b3ce-dae2-41ec-90ff-9ab49e0301bd">ITokenCollection</a> object that describes how the query was tokenized. This parameter can be <b>NULL</b>.
            


### -param plcid [out]

Type: <b>LCID*</b>


              Receives a LCID for the word breaker used for this query. This parameter can be <b>NULL</b>.
            


### -param ppWordBreaker [out]

Type: <b><a href="33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>


              Receives a pointer to the word breaker used for this query. This parameter can be <b>NULL</b>.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



