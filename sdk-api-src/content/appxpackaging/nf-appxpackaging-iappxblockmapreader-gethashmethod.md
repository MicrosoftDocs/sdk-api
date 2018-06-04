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

# IAppxBlockMapReader::GetHashMethod


## -description


Retrieves the URI for the hash algorithm used to create block hashes in the block map.


## -parameters




### -param hashMethod [out, retval]

Type: <b><a href="https://msdn.microsoft.com/a9e3688b-d64c-4396-9943-775971d2e739">IUri</a>**</b>

The hash algorithm used in this block map.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>hashMethod</i> value corresponds to the <b>HashMethod</b> attribute of the <a href="https://msdn.microsoft.com/75eed334-6c80-4eb3-8776-fc34d7aa5357">BlockMap</a> root element. 

<b>GetHashMethod</b> returns supported URIs for <a href="https://msdn.microsoft.com/de7b02d8-8d72-4e94-887f-5f319784e79b">DigestMethod</a>s.




## -see-also




<a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>
 

 

