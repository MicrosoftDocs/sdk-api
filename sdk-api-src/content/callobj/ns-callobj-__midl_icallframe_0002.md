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

# __MIDL_ICallFrame_0002 structure


## -description


Provides information about the parameter on the stack.


## -struct-fields




### -field fIn

<b>TRUE</b> if this is an [in] parameter; otherwise, <b>FALSE</b>.


### -field fOut

<b>TRUE</b> if this is an [out] parameter; otherwise, <b>FALSE</b>.


### -field stackOffset

Represents the offset in bytes from the stack location of the frame to the start of the parameter.


### -field cbParam

Represents the size in bytes occupied by the parameter on the stack.



## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

