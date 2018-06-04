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

# IRdcLibrary::ComputeDefaultRecursionDepth


## -description


The 
   <b>ComputeDefaultRecursionDepth</b> 
 method computes the maximum level of recursion for the specified file size. The depth returned 
 by the method may be larger than <b>MSRDC_MAXIMUM_DEPTH</b>. The caller must compare the value 
 returned through the <i>depth</i> parameter with 
 <b>MSRDC_MAXIMUM_DEPTH</b>.


## -parameters




### -param fileSize [in]

The approximate size of the file.


### -param depth [out]

Pointer to a <b>ULONG</b> that will receive the suggested maximum recursion 
    depth.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/941fa35c-20fa-4843-89be-26112ff7eec5">IRdcLibrary</a>
 

 

