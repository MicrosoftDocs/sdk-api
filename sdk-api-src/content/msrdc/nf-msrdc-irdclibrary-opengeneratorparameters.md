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

# IRdcLibrary::OpenGeneratorParameters


## -description


The <b>OpenGeneratorParameters</b> method 
    opens an existing serialized parameter block and returns an 
  <a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a> interface pointer initialized 
  with the data.


## -parameters




### -param size [in]

The size, in bytes, of the serialized parameter block.


### -param parametersBlob [in]

Pointer to a serialized parameter block.


### -param iGeneratorParameters [out]

Pointer to a location that will receive the returned 
    <a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a> interface pointer. Callers 
  must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To create a serialized parameter block, use the <a href="https://msdn.microsoft.com/ba0d09b0-417f-494a-a5e8-dccd08e5280a">IRdcGeneratorParameters::Serialize</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a>



<a href="https://msdn.microsoft.com/ba0d09b0-417f-494a-a5e8-dccd08e5280a">IRdcGeneratorParameters::Serialize</a>



<a href="https://msdn.microsoft.com/941fa35c-20fa-4843-89be-26112ff7eec5">IRdcLibrary</a>
 

 

