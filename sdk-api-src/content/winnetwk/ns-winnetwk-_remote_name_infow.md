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

# _REMOTE_NAME_INFOW structure


## -description


The <b>REMOTE_NAME_INFO</b> structure contains information about the remote form of a universal name. It is used by the 
<a href="https://msdn.microsoft.com/976b5910-c34f-49fa-b25e-82bf607e33a9">NPGetUniversalName</a> function.


## -struct-fields




### -field lpUniversalName

Pointer to the universal name if the provider supports universal names. Otherwise, this points to <b>NULL</b>.


### -field lpConnectionName

Pointer to a string containing the remote name used to make the connection. This string does not have a trailing backslash.


### -field lpRemainingPath

Pointer to the remaining path that must to be concatenated to a drive letter after a connection is established by means of <b>lpConnectionName</b>, to refer to the object specified during the call to <a href="https://msdn.microsoft.com/976b5910-c34f-49fa-b25e-82bf607e33a9">NPGetUniversalName</a>. This string has a backslash at the start of the path.

