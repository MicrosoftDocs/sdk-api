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

# IWICProgressiveLevelControl::GetCurrentLevel


## -description


Gets the decoder's current progressive level.


## -parameters




### -param pnLevel [out, retval]

Type: <b>UINT*</b>

Indicates the current level specified.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The level always defaults to the highest progressive level. In order to decode a lower progressive level, <a href="https://msdn.microsoft.com/b4a2c279-385d-4177-bd8f-a49f545c692a">SetCurrentLevel</a> must first be called.




## -see-also




<a href="https://msdn.microsoft.com/d77244bc-b9d4-4b7d-b718-4ee38de46614">IWICProgressiveLevelControl</a>



<a href="https://msdn.microsoft.com/d22c2c59-0fa1-4452-93f1-dbf151033714">Progressive Decoding Overview</a>
 

 

