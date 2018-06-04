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

# SaferIdentifyLevel function


## -description


The <b>SaferIdentifyLevel</b> function retrieves information about a level.


## -parameters




### -param dwNumProperties [in]

Number of 
<a href="https://msdn.microsoft.com/039a37a9-1744-4cff-919e-e0da50d7b291">SAFER_CODE_PROPERTIES</a> structures in the <i>pCodeproperties</i>  parameter.


### -param pCodeProperties [in, optional]

Array of <a href="https://msdn.microsoft.com/039a37a9-1744-4cff-919e-e0da50d7b291">SAFER_CODE_PROPERTIES</a> structures. Each structure contains a code file to be checked and the  criteria used to check the file.


### -param pLevelHandle [out]

The returned SAFER_LEVEL_HANDLE. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/8daffb35-5bb0-45b3-aff1-a8ea6a142ba5">SaferCloseLevel</a> function.


### -param lpReserved

Reserved for future use. Should be set to <b>NULL</b>.

Beginning with Windows 8 and Windows Server 2012 SRP_POLICY_APPX is defined as Windows Store app.


## -returns



<b>TRUE</b> if a SAFER_LEVEL_HANDLE was opened; otherwise,  <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



