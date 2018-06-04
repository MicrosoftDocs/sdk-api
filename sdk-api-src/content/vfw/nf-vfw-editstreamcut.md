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

# EditStreamCut function


## -description



The <b>EditStreamCut</b> function deletes all or part of an editable stream and creates a temporary editable stream from the deleted portion of the stream.




## -parameters




### -param pavi

Handle to the stream being edited.


### -param plStart

Starting position of the data to cut from the stream referenced by <i>pavi</i>.


### -param plLength

Amount of data to cut from the stream referenced by <i>pavi</i>.


### -param ppResult

Pointer to the handle created for the new stream.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



The stream being edited must have been created by the <b>CreateEditableStream</b> function or one of the stream editing functions.

The temporary stream is an editable stream and can be treated as any other AVI stream. An application must release the temporary stream to free the resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

