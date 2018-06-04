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

# IRdcSignatureReader::ReadHeader


## -description


The 
   <b>ReadHeader</b> method
   reads the signature header and returns a copy of the parameters
   used to generate the signatures.


## -parameters




### -param rdc_ErrorCode [out]

Address of a <a href="https://msdn.microsoft.com/32e9eab0-dc6e-4e04-af8a-bc2ed4adf0be">RDC_ErrorCode</a> enumeration that will 
      receive any RDC-specific error code.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dec6eb10-1243-4888-9ccc-ab1f4cfb11e7">IRdcSignatureReader</a>



<a href="https://msdn.microsoft.com/32e9eab0-dc6e-4e04-af8a-bc2ed4adf0be">RDC_ErrorCode</a>
 

 

