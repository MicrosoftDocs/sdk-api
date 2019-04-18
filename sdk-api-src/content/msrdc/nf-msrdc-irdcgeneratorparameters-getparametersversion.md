---
UID: NF:msrdc.IRdcGeneratorParameters.GetParametersVersion
title: IRdcGeneratorParameters::GetParametersVersion (msrdc.h)
author: windows-sdk-content
description: Returns information about the version of RDC used to serialize the parameters.
old-location: rdc\irdcgeneratorparameters_getparametersversion.htm
tech.root: rdc
ms.assetid: 58050740-0508-4797-b1b5-7a1e2a6dc00b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetParametersVersion, GetParametersVersion method [Remote Differential Compression], GetParametersVersion method [Remote Differential Compression],IRdcGeneratorParameters interface, IRdcGeneratorParameters interface [Remote Differential Compression],GetParametersVersion method, IRdcGeneratorParameters.GetParametersVersion, IRdcGeneratorParameters::GetParametersVersion, fs.irdcgeneratorparameters_getparametersversion, msrdc/IRdcGeneratorParameters::GetParametersVersion, rdc.irdcgeneratorparameters_getparametersversion
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsRdc.dll
req.lib: 
req.dll: MsRdc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcGeneratorParameters.GetParametersVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 

 

