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

# IWiaItemExtras::GetExtendedErrorInfo


## -description


The <b>IWiaItemExtras::GetExtendedErrorInfo</b> method gets a string from the device driver that contains information about the most recent error. Call this method after an error during an operation on a Windows Image Acquisition (WIA) item (such as data transfer).


## -parameters




### -param bstrErrorText [out]

Type: <b>BSTR*</b>

Pointer to a string that contains the error information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




Applications must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to free the string to which <i>bstrErrorText</i> points.





## -see-also




<a href="https://msdn.microsoft.com/b04f22dc-47d2-4434-82f9-4d6c618f31b3">IWiaItemExtras</a>
 

 

