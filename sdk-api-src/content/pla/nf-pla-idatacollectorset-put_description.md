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

# IDataCollectorSet::put_Description


## -description


Retrieves or sets the description of the data collector set.  The description will be added to all output files as metadata and inserted into Performance Data Helper logs as a comment.

This property is read/write.


## -parameters


## -remarks



To use a localized string from a binary, specify the description in the form @<i>binary</i>,#<i>id</i> where <i>binary</i> is the EXE or DLL that contains the localized resource string and <i>id</i> is the string resource identifier.

If you set the description to the @<i>binary</i>,#<i>id</i> form, when you retrieve  the description you will receive the localized string. To retrieve the description string that you set, access the <a href="https://msdn.microsoft.com/153159b2-54dc-477a-92eb-18328ea3351b">IDataCollectorSet::DescriptionUnresolved</a> property.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/153159b2-54dc-477a-92eb-18328ea3351b">IDataCollectorSet::DescriptionUnresolved</a>
 

 

