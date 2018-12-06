---
UID: NF:msrdc.IRdcGeneratorParameters.Serialize
title: IRdcGeneratorParameters::Serialize
author: windows-sdk-content
description: Serializes the parameter data into a block of memory.
old-location: rdc\irdcgeneratorparameters_serialize.htm
tech.root: rdc
ms.assetid: ba0d09b0-417f-494a-a5e8-dccd08e5280a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRdcGeneratorParameters interface [Remote Differential Compression],Serialize method, IRdcGeneratorParameters.Serialize, IRdcGeneratorParameters::Serialize, Serialize, Serialize method [Remote Differential Compression], Serialize method [Remote Differential Compression],IRdcGeneratorParameters interface, fs.irdcgeneratorparameters_serialize, msrdc/IRdcGeneratorParameters::Serialize, rdc.irdcgeneratorparameters_serialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRdcGeneratorParameters.Serialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRdcGeneratorParameters::Serialize


## -description


The 
   <b>Serialize</b> method serializes the 
   parameter data into a block of memory. This allows the parameters to be stored or transmitted.


## -parameters




### -param size [in]

The size of the buffer pointed to by the <i>parametersBlob</i> parameter.


### -param parametersBlob [out]

The address of a buffer to receive the serialized parameter data.


### -param bytesWritten [out]

Address of a <b>ULONG</b> that on successful completion is filled with the size, in 
      bytes, of the serialized parameter data written to the buffer pointed to by the 
      <i>parametersBlob</i> parameter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ebd41d6c-c321-4017-bcc1-a2cdf5202730">GetSerializeSize</a>



<a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a>
 

 

