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

# MsiRecordGetInteger function


## -description


The 
<b>MsiRecordGetInteger</b> function returns the integer value from a record field.


## -parameters




### -param hRecord [in]

Handle to a record.


### -param iField [in]

Specifies the field of the record from which to obtain the value.


## -returns



If the function succeeds, the return value is the integer value of the field.




## -remarks



The 
<b>MsiRecordGetInteger</b> function returns <b>MSI_NULL_INTEGER</b> if the field is null or if the field is a string that cannot be converted to an integer.




## -see-also




<a href="database_functions.htm">Record Processing Functions</a>
 

 

