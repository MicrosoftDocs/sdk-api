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

# IMFSensorTransformFactory::GetTransformInformation


## -description


Called by the media pipeline to get information about a transform provided by the  sensor transform.


## -parameters




### -param TransformIndex [in]

The index of the transform for which information is being requested. In the current release, this value will always be 0.


### -param pguidTransformId [out]

Gets the identifier for the transform.


### -param ppAttributes [out]

The attribute store to be populated.


### -param ppStreamInformation [out]

A collection of <a href="https://msdn.microsoft.com/9A5F6E25-796A-4798-8E4A-ABB9EB6A3B84">IMFSensorStream</a> objects.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/291EA582-22E3-4646-8E89-74162E98203F">IMFSensorTransformFactory</a>
 

 

