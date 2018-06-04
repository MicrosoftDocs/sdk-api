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

# PFNDAENUMCALLBACKCONST callback function


## -description


Defines the prototype for the callback function used by dynamic structure array (DSA) and dynamic pointer array (DPA) functions when the items involved are pointers to constant data.


## -parameters




### -param *p [in, optional]

Type: <b>const void*</b>

A pointer to the constant structure to be enumerated.


### -param *pData [in, optional]

Type: <b>void*</b>

A value that was passed in the <i>pData</i> parameter to function <a href="https://msdn.microsoft.com/31abb9f9-52b5-45d3-81e3-f9ccb5977597">DSA_EnumCallback</a> or function <a href="https://msdn.microsoft.com/25400c05-5f1d-46b6-b603-d33ed9bd24db">DPA_EnumCallback</a>.


## -returns



Type: <b>int</b>

The return value is used to determine whether to terminate or continue the iteration. A return value of zero indicates that the iteration should stop; nonzero indicates that the iteration should continue.




## -remarks



Alternate names for this callback are <b>PFNDPAENUMCALLBACKCONST</b> and <b>PFNDSAENUMCALLBACKCONST</b>.



