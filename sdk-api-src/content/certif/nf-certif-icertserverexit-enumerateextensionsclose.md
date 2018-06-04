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

# ICertServerExit::EnumerateExtensionsClose


## -description


The <b>EnumerateExtensionsClose</b>  method frees any resources connected with extension enumeration.

All applications that use <a href="https://msdn.microsoft.com/2a0c4919-b3a0-4027-85bd-970f6bc0cdeb">ICertServerExit::EnumerateExtensionsSetup</a> and <a href="https://msdn.microsoft.com/8726f5fa-dc85-4357-b73a-013842d6ab78">ICertServerExit::EnumerateExtensions</a> should call <b>EnumerateExtensionsClose</b> when finished enumerating.


## -parameters






## -see-also




<b>CCertServerExit</b>



<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>
 

 

