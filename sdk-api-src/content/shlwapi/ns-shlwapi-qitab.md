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

# QITAB structure


## -description


Used by the <a href="https://msdn.microsoft.com/8429778b-bc9c-43f6-8d75-0fb78e36e790">QISearch</a> function to describe a single interface.


## -struct-fields




### -field piid

Type: <b>const IID*</b>

A pointer to the IID of the interface represented by this structure.


### -field dwOffset

Type: <b>int</b>

The offset, in bytes, from the base of the object to the start of the interface.


## -remarks



<div class="alert"><b>Note</b>  Prior to Windows Vista, <b>QITAB</b> was not declared in a public header file. To use it in those cases, you must use define it yourself as it is given here. Under Windows Vista, <b>QITAB</b> is included in Shlwapi.h and this is not necessary.</div>
<div> </div>
To mark the end of a <b>QITAB</b> table, set the <b>piid</b> member to <b>NULL</b> and the <b>dwOffset</b> member to 0. See the <a href="https://msdn.microsoft.com/8429778b-bc9c-43f6-8d75-0fb78e36e790">QISearch</a> function for an example of how to use this structure.



