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

# IStream_Reset function


## -description


Moves the seek position in a specified stream to the beginning of the stream.


## -parameters




### -param pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface of the stream whose position is to be reset.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> on success or a COM failure code otherwise. See <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">IStream::Seek</a> for further discussion of possible error codes.




## -remarks



This function calls <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">IStream::Seek</a> to move the stream's seek position to the beginning of the stream.



