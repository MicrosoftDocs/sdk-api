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

# EngEnumForms function


## -description


The <b>EngEnumForms</b> function enumerates the forms supported by the specified printer.


## -parameters




### -param hPrinter [in]

Handle to the printer for which the forms should be enumerated. This is the PDEV handle that is passed as the <i>hDriver</i> parameter of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param Level [in]

Specifies the version of the structure pointed to by <i>pForm</i>. This value must be 1, which indicates that the enumerated forms are to be returned in FORM_1_INFO structures.


### -param pForm [out, optional]

Pointer to an array of bytes in which the enumerated FORM_INFO_1 structures are written.


### -param cbBuf [in]

Specifies the size, in bytes, of <i>lpbForms</i>.


### -param pcbNeeded [out]

Pointer to a DWORD that receives the number of bytes copied into <i>pForm </i>if the copy is completed successfully. If <i>pForm</i> is too small to contain all the enumerated forms' data, this DWORD specifies the number of bytes required.


### -param pcReturned [out]

Pointer to a DWORD that receives the number of FORM_INFO_1 structures copied into <i>pForm</i>.


## -returns



<b>EngEnumForms</b> returns <b>TRUE</b> if all parameters are valid and the enumerated form data is successfully copied into <i>pForm</i>. Otherwise, it returns <b>FALSE</b> and an error message is logged. To get error information, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564940">EngGetLastError</a>.




## -remarks



A printer driver can call <b>EngEnumForms</b> to have GDI obtain the list of forms supported by a particular printer. The enumerated information is returned as an array of FORM_INFO_1 structures (declared in the Microsoft Windows SDK documentation) pointed to by <i>pForm</i>. If the array pointed to by <i>pForm</i> is not large enough to hold the enumerated data, the requisite array size is instead returned in <i>pcbNeeded</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564940">EngGetLastError</a>
 

 

