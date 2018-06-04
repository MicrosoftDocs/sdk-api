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

# IWiaItemExtras::Escape


## -description


The <b>IWiaItemExtras::Escape</b> method sends a request for a vendor-specific I/O operation to a still image device.


## -parameters




### -param dwEscapeCode [in]

Type: <b>DWORD</b>

Calling application-supplied, vendor-defined, DWORD-sized value that represents an I/O operation.


### -param lpInData [in]

Type: <b>BYTE*</b>

Pointer to a calling application-supplied buffer that contains data to be sent to the device.


### -param cbInDataSize [in]

Type: <b>DWORD</b>

Calling application-supplied length, in bytes, of the data contained in the buffer pointed to by <i>lpInData</i>.


### -param pOutData [out]

Type: <b>BYTE*</b>

Pointer to a calling application-supplied memory buffer to receive data from the device.


### -param dwOutDataSize [in]

Type: <b>DWORD</b>

Calling application-supplied length, in bytes, of the buffer pointed to by <i>pOutData</i>.


### -param pdwActualDataSize [out]

Type: <b>DWORD*</b>

Receives the number of bytes actually written to <i>pOutData</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b04f22dc-47d2-4434-82f9-4d6c618f31b3">IWiaItemExtras</a>
 

 

