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

# _FILTERED_DATA_SOURCES structure


## -description


Specifies parameters for a Shell data source for which a filter is loaded.


## -struct-fields




### -field pwcsExtension

Pointer to a buffer that contains a file name extension.


### -field pwcsMime

Pointer to a buffer that contains the name of a MIME type.


### -field pClsid

Pointer to a CLSID that identifies the content type. 


### -field pwcsOverride

Not implemented.


## -remarks



A filter, also known as a filter handler, is an implementation of the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface.

<b>FILTERED_DATA_SOURCES</b> can hold one file content identifier of each type. CLSIDs are always searched first, followed by the  file name extension, then MIME type, and finally the path. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7b24986b-972d-4674-846b-f856b908edf4">Developing Filter Handlers</a>



<a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>



<a href="https://msdn.microsoft.com/7ac51909-fa0e-4f97-8da0-0ab4c5de7d60">ILoadFilter</a>



<b>Reference</b>
 

 

