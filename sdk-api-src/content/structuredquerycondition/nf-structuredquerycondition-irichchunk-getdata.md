---
UID: NF:structuredquerycondition.IRichChunk.GetData
title: IRichChunk::GetData
author: windows-sdk-content
description: Retrieves the PROPVARIANT and input string that represents a chunk of data.
old-location: search\_search_IRichChunk_GetData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irichchunk\getdata.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetData, GetData method [search], GetData method [search],IRichChunk interface, IRichChunk interface [search],GetData method, IRichChunk.GetData, IRichChunk::GetData, _search_IRichChunk_GetData, search._search_IRichChunk_GetData, structuredquerycondition/IRichChunk::GetData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: structuredquerycondition.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: StructuredQueryCondition.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - StructuredQueryCondition.h
api_name:
 - IRichChunk.GetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
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
 

 

