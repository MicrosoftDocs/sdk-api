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

# _tagSYNCMGRLOGLEVEL enumeration


## -description


The 
<b>SYNCMGRLOGLEVEL</b> enumeration values specify an error level for use in the 
<a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">ISyncMgrSynchronizeCallback::LogError</a> method.


## -enum-fields




### -field SYNCMGRLOGLEVEL_INFORMATION

An information message was logged.


### -field SYNCMGRLOGLEVEL_WARNING

A warning message was logged.


### -field SYNCMGRLOGLEVEL_ERROR

An error message was logged.


### -field SYNCMGRLOGLEVEL_LOGLEVELMAX

The largest valid <a href="https://msdn.microsoft.com/df3c3300-e203-4664-b8d5-9dc4835b33d8">SYNCMGRLOGLEVEL</a> value.


## -see-also




<a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">ISyncMgrSynchronizeCallback::LogError</a>
 

 

