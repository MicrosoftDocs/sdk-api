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

# IRdcGeneratorParameters::GetParametersVersion


## -description


The <b>GetParametersVersion</b> 
    method returns information about the version of RDC used to serialize the parameters.


## -parameters




### -param currentVersion [out]

Address of a <b>ULONG</b> that will receive the version of RDC used to serialize the 
      parameters for this object. This corresponds to the <b>MSRDC_VERSION</b> constant.


### -param minimumCompatibleAppVersion [out]

Address of a <b>ULONG</b> that will receive the version of RDC that is compatible 
      with the serialized parameters. This corresponds to the 
      <b>MSRDC_MINIMUM_COMPATIBLE_APP_VERSION</b> constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a>



<a href="https://msdn.microsoft.com/3eef00e8-62d9-49bc-8340-fb56f5a4573d">IRdcLibrary::GetRDCVersion</a>
 

 

