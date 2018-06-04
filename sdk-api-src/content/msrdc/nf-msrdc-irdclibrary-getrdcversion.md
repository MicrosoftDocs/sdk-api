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

# IRdcLibrary::GetRDCVersion


## -description


The <b>GetRDCVersion</b> method retrieves 
    the version of the installed RDC runtime and the oldest version of the RDC interfaces supported by the installed 
    runtime.


## -parameters




### -param currentVersion [out]

Address of a <b>ULONG</b> that will receive the installed version of RDC. This 
      corresponds to the <b>MSRDC_VERSION</b> value.


### -param minimumCompatibleAppVersion [out]

Address of a <b>ULONG</b> that will receive the oldest version of RDC supported by 
      the installed version of RDC. This corresponds to the 
      <b>MSRDC_MINIMUM_COMPATIBLE_APP_VERSION</b> value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/58050740-0508-4797-b1b5-7a1e2a6dc00b">IRdcGeneratorParameters::GetParametersVersion</a>



<a href="https://msdn.microsoft.com/941fa35c-20fa-4843-89be-26112ff7eec5">IRdcLibrary</a>
 

 

