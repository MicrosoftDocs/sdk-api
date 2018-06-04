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

# PFXIsPFXBlob function


## -description



			The <b>PFXIsPFXBlob</b> function attempts to decode the outer layer of a BLOB as a PFX packet.


## -parameters




### -param pPFX [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that the function will attempt to decode as a PFX packet.


## -returns



The function returns <b>TRUE</b> if the BLOB can be decoded as a PFX packet. If the outer layer of the BLOB cannot be decoded as a PFX packet, the function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/47560192-547e-4440-9f10-43327355e1a0">PFXVerifyPassword</a>
 

 

