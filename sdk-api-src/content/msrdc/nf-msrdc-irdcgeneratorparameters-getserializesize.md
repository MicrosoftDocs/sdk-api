---
UID: NF:msrdc.IRdcGeneratorParameters.GetSerializeSize
title: IRdcGeneratorParameters::GetSerializeSize
author: windows-sdk-content
description: Returns the size, in bytes, of the serialized parameter data.
old-location: rdc\irdcgeneratorparameters_getserializesize.htm
old-project: Rdc
ms.assetid: ebd41d6c-c321-4017-bcc1-a2cdf5202730
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetSerializeSize, GetSerializeSize method [Remote Differential Compression], GetSerializeSize method [Remote Differential Compression],IRdcGeneratorParameters interface, IRdcGeneratorParameters interface [Remote Differential Compression],GetSerializeSize method, IRdcGeneratorParameters.GetSerializeSize, IRdcGeneratorParameters::GetSerializeSize, fs.irdcgeneratorparameters_getserializesize, msrdc/IRdcGeneratorParameters::GetSerializeSize, rdc.irdcgeneratorparameters_getserializesize
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
 - IRdcGeneratorParameters.GetSerializeSize
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a>



<a href="https://msdn.microsoft.com/ba0d09b0-417f-494a-a5e8-dccd08e5280a">Serialize</a>
 

 

