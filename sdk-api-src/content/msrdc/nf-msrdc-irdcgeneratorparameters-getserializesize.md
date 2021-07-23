---
UID: NF:msrdc.IRdcGeneratorParameters.GetSerializeSize
title: IRdcGeneratorParameters::GetSerializeSize (msrdc.h)
description: Returns the size, in bytes, of the serialized parameter data.
helpviewer_keywords: ["GetSerializeSize","GetSerializeSize method [Remote Differential Compression]","GetSerializeSize method [Remote Differential Compression]","IRdcGeneratorParameters interface","IRdcGeneratorParameters interface [Remote Differential Compression]","GetSerializeSize method","IRdcGeneratorParameters.GetSerializeSize","IRdcGeneratorParameters::GetSerializeSize","fs.irdcgeneratorparameters_getserializesize","msrdc/IRdcGeneratorParameters::GetSerializeSize","rdc.irdcgeneratorparameters_getserializesize"]
old-location: rdc\irdcgeneratorparameters_getserializesize.htm
tech.root: rdc
ms.assetid: ebd41d6c-c321-4017-bcc1-a2cdf5202730
ms.date: 12/05/2018
ms.keywords: GetSerializeSize, GetSerializeSize method [Remote Differential Compression], GetSerializeSize method [Remote Differential Compression],IRdcGeneratorParameters interface, IRdcGeneratorParameters interface [Remote Differential Compression],GetSerializeSize method, IRdcGeneratorParameters.GetSerializeSize, IRdcGeneratorParameters::GetSerializeSize, fs.irdcgeneratorparameters_getserializesize, msrdc/IRdcGeneratorParameters::GetSerializeSize, rdc.irdcgeneratorparameters_getserializesize
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
 - IRdcGeneratorParameters::GetSerializeSize
 - msrdc/IRdcGeneratorParameters::GetSerializeSize
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
 - IRdcGeneratorParameters.GetSerializeSize
---

# IRdcGeneratorParameters::GetSerializeSize


## -description

The <b>GetSerializeSize</b> method 
    returns the size, in bytes, of the serialized parameter data.

## -parameters

### -param size [out]

Address of a <b>ULONG</b> that on successful completion is filled with the size, in 
      bytes, of the serialized parameter data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorparameters-serialize">Serialize</a>