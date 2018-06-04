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

# STROBJ_vEnumStart function


## -description


The <b>STROBJ_vEnumStart</b> function defines the form, or type, for data that will be returned from GDI in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff569739">STROBJ_bEnum</a>. 


## -parameters




### -param pstro

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a> structure whose data form is to be defined.


## -returns



None




## -remarks



This function also restarts the enumeration of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a> array.

This function should be called by the driver prior to calling <b>STROBJ_bEnum</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569739">STROBJ_bEnum</a>
 

 

