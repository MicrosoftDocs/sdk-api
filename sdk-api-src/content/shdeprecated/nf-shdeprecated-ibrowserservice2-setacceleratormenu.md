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

# IBrowserService2::SetAcceleratorMenu


## -description


Deprecated. Implemented by a derived class to define menu accelerators that can be used in a call to <a href="https://msdn.microsoft.com/dda5c085-7199-4b83-b03e-e4c715665157">TranslateAcceleratorSB</a>.


## -parameters




### -param hacc [in]

Type: <b>HACCEL</b>


          A handle to an array of <a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a> structures, each structure describing a keyboard mnemonic.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



