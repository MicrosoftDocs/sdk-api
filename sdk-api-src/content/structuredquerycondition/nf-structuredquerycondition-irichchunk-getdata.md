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

# IRichChunk::GetData


## -description



      Retrieves the <a href="_stg_propvariant">PROPVARIANT</a> and input string that represents a chunk of data.


## -parameters




### -param pFirstPos [out]

Type: <b>ULONG*</b>


          Receives the zero-based starting position of the range. This parameter can be <b>NULL</b>.
        


### -param pLength [out]

Type: <b>ULONG*</b>


          Receives the length of the range. This parameter can be <b>NULL</b>.
        


### -param ppsz [out]

Type: <b>LPWSTR*</b>


          Receives the associated Unicode string value, or <b>NULL</b> if not available.
        


### -param pValue [out]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>


          Receives the associated <a href="_stg_propvariant">PROPVARIANT</a> value, or <b>VT_EMPTY</b> if not available. This parameter can be <b>NULL</b>.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Prior to Windows 7, this was declared in structuredquery.idl and structuredquery.h.




## -see-also




<a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a>
 

 

