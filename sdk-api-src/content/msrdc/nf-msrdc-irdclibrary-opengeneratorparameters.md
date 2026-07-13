---
UID: NF:msrdc.IRdcLibrary.OpenGeneratorParameters
title: IRdcLibrary::OpenGeneratorParameters (msrdc.h)
description: Opens an existing serialized parameter block and returns an IRdcGeneratorParameters interface pointer initialized with the data.
helpviewer_keywords: ["IRdcLibrary interface [Remote Differential Compression]","OpenGeneratorParameters method","IRdcLibrary.OpenGeneratorParameters","IRdcLibrary::OpenGeneratorParameters","OpenGeneratorParameters","OpenGeneratorParameters method [Remote Differential Compression]","OpenGeneratorParameters method [Remote Differential Compression]","IRdcLibrary interface","fs.irdclibrary_opengeneratorparameters","msrdc/IRdcLibrary::OpenGeneratorParameters","rdc.irdclibrary_opengeneratorparameters"]
old-location: rdc\irdclibrary_opengeneratorparameters.htm
tech.root: rdc
ms.assetid: 6fbced31-a230-44d4-a9ee-bb3e15df2563
ms.date: 12/05/2018
ms.keywords: IRdcLibrary interface [Remote Differential Compression],OpenGeneratorParameters method, IRdcLibrary.OpenGeneratorParameters, IRdcLibrary::OpenGeneratorParameters, OpenGeneratorParameters, OpenGeneratorParameters method [Remote Differential Compression], OpenGeneratorParameters method [Remote Differential Compression],IRdcLibrary interface, fs.irdclibrary_opengeneratorparameters, msrdc/IRdcLibrary::OpenGeneratorParameters, rdc.irdclibrary_opengeneratorparameters
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRdcLibrary::OpenGeneratorParameters
 - msrdc/IRdcLibrary::OpenGeneratorParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcLibrary.OpenGeneratorParameters
---

# IRdcLibrary::OpenGeneratorParameters


## -description

The <b>OpenGeneratorParameters</b> method 
    opens an existing serialized parameter block and returns an 
  <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a> interface pointer initialized 
  with the data.

## -parameters

### -param size [in]

The size, in bytes, of the serialized parameter block.

### -param parametersBlob [in]

Pointer to a serialized parameter block.

### -param iGeneratorParameters [out]

Pointer to a location that will receive the returned 
    <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a> interface pointer. Callers 
  must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To create a serialized parameter block, use the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorparameters-serialize">IRdcGeneratorParameters::Serialize</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorparameters-serialize">IRdcGeneratorParameters::Serialize</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdclibrary">IRdcLibrary</a>