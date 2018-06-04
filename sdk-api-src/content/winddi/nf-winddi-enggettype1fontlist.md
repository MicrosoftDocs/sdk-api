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

# EngGetType1FontList function


## -description


The <b>EngGetType1FontList</b> function retrieves a list of PostScript Type 1 fonts that are installed both locally and remotely.


## -parameters




### -param hdev [in]

Handle to the device. This is the GDI handle received by the driver as the <i>hdev</i> parameter for <a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a>.


### -param pType1Buffer [out, optional]

Pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff570102">TYPE1_FONT</a> structures in which to store the Type 1 font list. This parameter can be <b>NULL</b>.


### -param cjType1Buffer [in]

Specifies the size, in bytes, of <i>pType1Buffer</i>.


### -param pulLocalFonts [out]

Pointer to a memory location that receives the number of Type 1 fonts on the local system.


### -param pulRemoteFonts [out]

Pointer to a memory location that receives the number of Type 1 fonts on the remote system.


### -param pLastModified [out]

Pointer to a memory location that receives the time stamp corresponding to the last time a Type 1 font was added or removed from the local system.


## -returns



<b>EngGetType1FontList</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



PostScript printer drivers can call <b>EngGetType1FontList</b> to obtain a list of Type 1 fonts available to them. These fonts can then be accessed through the handles returned in the TYPE1_FONT structure.

If <i>pType1Buffer</i> is <b>NULL</b>, <b>EngGetType1FontList</b> returns only the number of local and remote Type 1 fonts, as well as the time stamp corresponding to the last time a Type 1 font was added or removed locally from the system.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570102">TYPE1_FONT</a>
 

 

