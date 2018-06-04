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

# SLAcquireGenuineTicket function


## -description


Gets a XrML genuine ticket acquired from the Software Licensing Server (SLS).


## -parameters




### -param ppTicketBlob [out]

The address of a pointer to a buffer that receives the ticket BLOB. When you have finished using this buffer, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


### -param pcbTicketBlob [out]

A pointer to the size, in bytes, of the <i>ppTicketBlob</i> buffer.


### -param pwszTemplateId [in]

A pointer to a null-terminated string that contains the ID of the BLOB template stored on the SLS.


### -param pwszServerUrl [in]

A pointer to a null-terminated string that contains the URL of the SLS.


### -param pwszClientToken [in, optional]

Reserved.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



