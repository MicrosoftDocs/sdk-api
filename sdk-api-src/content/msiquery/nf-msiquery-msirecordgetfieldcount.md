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

# MsiRecordGetFieldCount function


## -description


The 
<b>MsiRecordGetFieldCount</b> function returns the number of fields in a record.


## -parameters




### -param hRecord [in]

Handle to a record.


## -returns



If the function succeeds, the return value is the number of fields in the record.




## -remarks



The count returned by the 
<b>MsiRecordGetFieldCount</b> parameter does not include field 0. Read access to fields beyond this count returns null values. Write access fails.




## -see-also




<a href="database_functions.htm">Record Processing Functions</a>
 

 

