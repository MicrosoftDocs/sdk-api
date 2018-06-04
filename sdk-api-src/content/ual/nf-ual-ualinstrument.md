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

# UalInstrument function


## -description


Records the specified data to the  User Access Logging (UAL) framework by using information from a <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure.

You must call the <a href="https://msdn.microsoft.com/800E8BCF-39A1-490A-9B6A-12EE900B8D17">UalStart</a> function before calling the <b>UalInstrument</b> function. When you have finished calling this function, call the <a href="https://msdn.microsoft.com/142A0C96-2D53-4C31-9847-D6D5313C841E">UalStop</a> function to clean up resources.


## -parameters




### -param Data [in]

A pointer to a <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure that specifies session information.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/800E8BCF-39A1-490A-9B6A-12EE900B8D17">UalStart</a>



<a href="https://msdn.microsoft.com/142A0C96-2D53-4C31-9847-D6D5313C841E">UalStop</a>
 

 

