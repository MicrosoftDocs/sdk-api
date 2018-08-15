---
UID: NF:msrdc.IRdcLibrary.OpenGeneratorParameters
title: IRdcLibrary::OpenGeneratorParameters
author: windows-sdk-content
description: Opens an existing serialized parameter block and returns an IRdcGeneratorParameters interface pointer initialized with the data.
old-location: rdc\irdclibrary_opengeneratorparameters.htm
old-project: Rdc
ms.assetid: 6fbced31-a230-44d4-a9ee-bb3e15df2563
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IRdcLibrary interface [Remote Differential Compression],OpenGeneratorParameters method, IRdcLibrary.OpenGeneratorParameters, IRdcLibrary::OpenGeneratorParameters, OpenGeneratorParameters, OpenGeneratorParameters method [Remote Differential Compression], OpenGeneratorParameters method [Remote Differential Compression],IRdcLibrary interface, fs.irdclibrary_opengeneratorparameters, msrdc/IRdcLibrary::OpenGeneratorParameters, rdc.irdclibrary_opengeneratorparameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcLibrary.OpenGeneratorParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

