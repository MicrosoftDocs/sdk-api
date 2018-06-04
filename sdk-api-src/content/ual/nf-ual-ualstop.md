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

# UalStop function


## -description


Stops a User Access Logging (UAL) session.


## -parameters




### -param Data [in]

A pointer to an <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure that specifies session information.

Only the <b>RoleGuid</b> property of the <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure is required. All other members can be null.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/C7A0340F-3250-4570-9672-FC78AFC9ECC6">UalInstrument</a>



<a href="https://msdn.microsoft.com/800E8BCF-39A1-490A-9B6A-12EE900B8D17">UalStart</a>
 

 

