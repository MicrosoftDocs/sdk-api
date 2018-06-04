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
 

 

