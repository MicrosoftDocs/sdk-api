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

# CryptSIPAddProvider function


## -description


The <b>CryptSIPAddProvider</b> function registers functions that are exported by a given DLL file that implements  a Subject Interface Package (SIP).


## -parameters




### -param psNewProv [in]

A pointer to a <a href="https://msdn.microsoft.com/5ca88c0c-a7c9-4517-a874-49d38c1bc7c3">SIP_ADD_NEWPROVIDER</a> structure that specifies the DLL file and function names to register.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails. If the function fails, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to determine the reason for failure.




## -remarks



Typically, you call this function as part of an in-process COM server registration. The <b>CryptSIPAddProvider</b> function persists the appropriate Registry entries for the SIP provider functions.

When you have finished using the added SIP provider, remove it by calling the <a href="https://msdn.microsoft.com/0a269956-b2c7-414a-b002-7cec0d52bfd6">CryptSIPRemoveProvider</a> function.




## -see-also




<a href="https://msdn.microsoft.com/0a269956-b2c7-414a-b002-7cec0d52bfd6">CryptSIPRemoveProvider</a>
 

 

