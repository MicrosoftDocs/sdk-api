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

# IBDA_FDC::GetTableSection


## -description


Gets the latest table section.


## -parameters




### -param Pid [out]

Receives the packet identifier (PID) of the table.


### -param MaxBufferSize [in]

The size of the <i>SecBuffer</i> array, in bytes.


### -param ActualSize [out]

Receives the number of bytes that the method copies into the  <i>SecBuffer</i> array.


### -param SecBuffer [out]

A byte array, allocated by the caller, that receives the table section.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8b7a07fd-99e9-4f8e-9211-109689f2f892">IBDA_FDC</a>
 

 

