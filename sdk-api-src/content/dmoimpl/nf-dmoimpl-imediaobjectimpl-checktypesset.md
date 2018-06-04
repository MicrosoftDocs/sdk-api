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

# IMediaObjectImpl::CheckTypesSet


## -description



The <code>CheckTypesSet</code> method determines whether the media type has been set on all of the streams.




## -parameters






## -returns



Returns <b>TRUE</b> if the media type has been set on all of the non-optional streams. Otherwise, returns <b>FALSE</b>.




## -remarks



Call this method after any operation that changes the media type on a stream. This method sets a private flag within the class. Some <b>IMediaObjectImpl</b> methods test this flag to determine whether certain operations are permitted. These methods generally return DMO_E_TYPE_NOT_SET if the flag is <b>FALSE</b>.

The only two methods in <b>IMediaObject</b> that change the media type on a stream are <b>SetInputType</b> and <b>SetOutputType</b>. The class template implements both of these methods.




## -see-also




<a href="https://msdn.microsoft.com/81d45b8d-8373-4e42-b768-f6126feb935d">IMediaObjectImpl Class Template</a>
 

 

