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

# IQuerySolution::GetErrors


## -description



          Identifies parts of the input string that the parser did not recognize or did not use when constructing the <a href="https://msdn.microsoft.com/a4987e80-7ad9-400d-8c6d-ec3b9a6bf3f1">IQuerySolution</a> condition tree.
        


## -parameters




### -param riid [in]

Type: <b>REFIID</b>


          The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.
        


### -param ppParseErrors [out, retval]

Type: <b>void**</b>


          Receives a pointer to an enumeration of zero or more <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> objects, each describing one parsing error.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 
        Each parsing error is represented by an <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> object in which the position information reflects token counts. The <b>IRichChunk</b> object <i>ppsz</i> string is <b>NULL</b>, and the <i>pValue</i> is a <a href="_stg_propvariant">PROPVARIANT</a> that contains a <b>lVal</b> identifying the <a href="https://msdn.microsoft.com/abc76a8c-ee72-469a-85a0-75c12ee4e5d9">STRUCTURED_QUERY_PARSE_ERROR</a> enumeration.
      


        The valid values for <i>riid</i> are __uuidof(IEnumUnknown) and __uuidof(IEnumVARIANT).
      



