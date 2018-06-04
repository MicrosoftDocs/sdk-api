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

# EngGetPrinterData function


## -description


The <b>EngGetPrinterData </b>function retrieves configuration data for the specified printer.


## -parameters




### -param hPrinter [in]

Handle to the printer for which configuration data should be retrieved. This is the handle that is passed as the <i>hDriver</i> parameter of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param pValueName [in]

Pointer to a null-terminated string that identifies the data to be retrieved.


### -param pType [out, optional]

Pointer to a variable that receives the data type stored by <a href="https://msdn.microsoft.com/library/windows/hardware/ff565020">EngSetPrinterData</a>. This parameter can be <b>NULL</b>.


### -param pData [out, optional]

Pointer to an array of bytes in which the configuration data is written.


### -param nSize [in]

Specifies the size, in bytes, of <i>pData</i>.


### -param pcbNeeded [out]

Pointer to a memory location that receives the number of bytes copied into <i>lpbData</i> if the function succeeds. This parameter receives the number of bytes required if <i>nSizef</i> is too small.


## -returns



<b>EngGetPrinterData</b> returns the last logged error message.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565020">EngSetPrinterData</a>
 

 

