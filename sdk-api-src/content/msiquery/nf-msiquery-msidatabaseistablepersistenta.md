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

# MsiDatabaseIsTablePersistentA function


## -description


The 
<b>MsiDatabaseIsTablePersistent</b> function returns an enumeration that describes the state of a specific table.


## -parameters




### -param hDatabase [in]

Handle to the database that belongs to the relevant table. For more information, see <a href="https://msdn.microsoft.com/53cf73bc-4d52-471c-8384-46d106a36e38">Obtaining a Database Handle</a>.


### -param szTableName [in]

Specifies the name of the relevant table.


## -returns



This function returns MSICONDITION.




## -see-also




<a href="database_functions.htm">General Database Access Functions</a>
 

 

