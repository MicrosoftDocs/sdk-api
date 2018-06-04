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

# IEnumWIA_FORMAT_INFO::Next


## -description


The <b>IEnumWIA_FORMAT_INFO::Next</b> method returns an array of <a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a> structures.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of elements requested. 


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a>*</b>

Receives the address of the array of <a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a> structures.


### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

On output, receives the address of a <b>ULONG</b> that contains the number of <a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a> structures actually returned in the <i>rgelt</i> parameter.


## -returns



Type: <b>HRESULT</b>

If the enumeration is continuing, this method returns S_OK and sets the value pointed to by <i>pceltFetched</i> to the number of capabilities returned. If the enumeration is complete, it returns S_FALSE and sets the value pointed to by <i>pceltFetched</i> to zero. If the method fails, it returns a standard COM error.



