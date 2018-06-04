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

# IFsrmPropertyBag2::GetFieldValue


## -description


Gets the value of the specified field from the property bag.


## -parameters




### -param field [in]

Type: <b><a href="https://msdn.microsoft.com/7a8cd6a6-7933-4190-b4fc-1b1cd653bd14">FsrmPropertyBagField</a></b>

Indicates whether the volume name returned is the name of the volume being accessed, which may be a snapshot, or the volume where the property bag lives.


### -param value [out, retval]

Type: <b>VARIANT*</b>

Returns the specified value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7a8cd6a6-7933-4190-b4fc-1b1cd653bd14">FsrmPropertyBagField</a>



<a href="https://msdn.microsoft.com/8f69556f-b96e-49b5-bc40-242768ebe767">IFsrmPropertyBag2</a>
 

 

