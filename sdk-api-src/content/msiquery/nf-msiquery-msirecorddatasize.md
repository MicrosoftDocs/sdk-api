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

# MsiRecordDataSize function


## -description


The 
<b>MsiRecordDataSize</b> function returns the length of a record field. The count does not include the terminating null character.


## -parameters




### -param hRecord [in]

Handle to the record.


### -param iField [in]

Specifies a field of the record.


## -returns



The 
<b>MsiRecordDataSize</b> function returns 0 if the field is null, nonexistent, or an internal object pointer. The function also returns 0 if the handle is not a valid record handle.

If the data is in integer format, the function returns sizeof(int).

If the data is in string format, the function returns the character count (not including the null character).

If the data is in stream format, the function returns the byte count.




## -see-also




<a href="database_functions.htm">Record Processing Functions</a>
 

 

