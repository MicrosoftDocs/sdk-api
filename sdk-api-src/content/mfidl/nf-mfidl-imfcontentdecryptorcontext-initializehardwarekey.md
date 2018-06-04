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

# IMFContentDecryptorContext::InitializeHardwareKey


## -description


 Allows the display driver to return IHV-specific information used when initializing a new hardware key. 


## -parameters




### -param InputPrivateDataByteCount [in]

The number of bytes in the buffer that <i>InputPrivateData</i> specifies.


### -param InputPrivateData [in, optional]

The contents of this parameter are defined by the implementation of   
         the protection system that runs in the security processor. The contents may contain data about license or stream properties.


### -param OutputPrivateData [out]

The return data is also defined by the implementation of the protection system implementation   
     that runs in the security processor.  The contents may contain data associated with the underlying hardware key.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94DB835F-3D2A-4CC8-A1CF-10215E3D30D6">IMFContentDecryptorContext</a>
 

 

