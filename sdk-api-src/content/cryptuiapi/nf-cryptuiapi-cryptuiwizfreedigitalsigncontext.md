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

# CryptUIWizFreeDigitalSignContext function


## -description


The <b>CryptUIWizFreeDigitalSignContext</b> function frees the <a href="https://msdn.microsoft.com/3e4eb745-0c28-4ce5-870b-d24565ef0cae">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a> structure allocated by the <a href="https://msdn.microsoft.com/1d01523e-d47b-49be-82c8-5e98f97be800">CryptUIWizDigitalSign</a> function.


## -parameters




### -param pSignContext [in]

A pointer to the   <a href="https://msdn.microsoft.com/3e4eb745-0c28-4ce5-870b-d24565ef0cae">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a> structure to be freed.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero.




## -see-also




<a href="https://msdn.microsoft.com/3e4eb745-0c28-4ce5-870b-d24565ef0cae">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a>



<a href="https://msdn.microsoft.com/1d01523e-d47b-49be-82c8-5e98f97be800">CryptUIWizDigitalSign</a>
 

 

