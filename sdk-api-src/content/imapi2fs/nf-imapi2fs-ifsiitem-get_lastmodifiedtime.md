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

# IFsiItem::get_LastModifiedTime


## -description


Retrieves the date and time that the directory or file item was last modified in the file system image.


## -parameters




### -param pVal [out]

Date and time that the directory or file  item was last modified in the file system image, according to UTC time.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



When implementing this method, a few things should be taken into consideration:

UDFS (UDF) will use the value provided by <a href="https://msdn.microsoft.com/11491b16-0bdc-41a6-a99d-0543cdc3bb64">IFsiItem::put_LastModifiedTime</a> as both the <i>CreationTime</i> and <i>LastModifiedTime</i>.

CDFS (ISO 9660) uses the date/time of recording as the <i>CreationTime</i> and <i>LastModifiedTime</i>. As a result, CDFS sets the value of <i>LastModifiedTime</i> to 0.




## -see-also




<a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a>



<a href="https://msdn.microsoft.com/11491b16-0bdc-41a6-a99d-0543cdc3bb64">IFsiItem::put_LastModifiedTime</a>
 

 

