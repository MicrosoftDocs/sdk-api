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

# EngGetForm function


## -description


The <b>EngGetForm</b> function gets the FORM_INFO_1 details for the specified form.


## -parameters




### -param hPrinter [in]

Handle to the printer for which the form is being specified.


### -param pFormName [in]

Pointer to a string that specifies the name of the form.


### -param Level [in]

Specifies the version of the form structure to which <i>pForm</i> points. This value must be 1, which indicates that the form information will be returned in a FORM_INFO_1 structure.


### -param pForm [in, optional]

Pointer to an array of bytes that receives the initialized FORM_INFO_1 structure.


### -param cbBuf [in]

Specifies the size, in bytes, of <i>pForm</i>.


### -param pcbNeeded [out]

Pointer to a value that specifies the number of bytes copied into the buffer pointed to by <i>pForm</i> if the function succeeds. The value is the number of bytes required to perform the copy if <i>cbBuf</i> is too small.


## -returns



<b>EngGetForm</b> returns <b>TRUE</b> if the form structure is successfully copied into <i>pForm</i>. Otherwise, it logs an error message and returns <b>FALSE</b>. To get the error information, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564940">EngGetLastError</a>.




## -remarks



<b>EngGetForm</b> returns a FORM_INFO_1 structure (described in the Microsoft Windows SDK documentation) containing the form data associated with <i>pFormName</i>. The written data and its size are returned to the caller via <i>pForm</i> and <i>pcbNeeded</i>, respectively. If the array pointed to by <i>pForm</i> is not large enough to hold the form data, the requisite array size is instead returned in <i>pcbNeeded</i>.

To get a list of all supported forms, the printer driver should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564850">EngEnumForms</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564850">EngEnumForms</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564940">EngGetLastError</a>
 

 

