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

# IFsiItem::get_LastAccessedTime


## -description


Retrieves the date and time the directory or file item was last accessed in the file system image.


## -parameters




### -param pVal [out]

Date and time that the item directory or file was last accessed in the file system image, according to UTC time.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



UDFS (UDF) uses the <i>LastAccessedTime</i> value for the <i>CreationTime</i>, as IMAPI does not currently support the <i>CreationTime</i> extended attribue.

CDFS (ISO 9660) sets the <i>LastAccessedTime</i> value retrieved by this method to 0, as only the recording time is stored within the File/Directory descriptor.




## -see-also




<a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a>



<a href="https://msdn.microsoft.com/6192bff5-9535-4845-9c99-d5ceeea0335f">IFsiItem::put_LastAccessedTime</a>
 

 

