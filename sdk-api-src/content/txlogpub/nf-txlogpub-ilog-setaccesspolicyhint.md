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

# ILog::SetAccessPolicyHint


## -description


Provides a hint to the implementation about the pattern in which records will be read.


## -parameters




### -param policy [in]

The pattern in which records will most often be read. For more information, see the <a href="https://msdn.microsoft.com/79ffd37a-ffeb-46f8-8743-aa3e85648e34">RECORD_READING_POLICY</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Not all implementations of <a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a> will be optimized for reading records in a particular pattern. An implementation may choose to ignore this request and return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a>



<a href="https://msdn.microsoft.com/79ffd37a-ffeb-46f8-8743-aa3e85648e34">RECORD_READING_POLICY</a>
 

 

