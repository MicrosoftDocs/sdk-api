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

# __MIDL_ItsPubPlugin2_0001 structure


## -description


Contains information about a file association in RemoteApp and Desktop Connection.


## -struct-fields




### -field extName

A null-terminated string that contains the file name extension. The length of this string is limited to <b>MAX_FILE_ASSOC_EXTENSION_SIZE</b> characters, including the terminating <b>NULL</b> character.


### -field primaryHandler

Indicates if this is the primary handler for the file association.


### -field pceIconSize

The size, in bytes, of the <b>iconContents</b> buffer.


### -field iconContents

A byte array that contains the icon to display for files with the specified extension.


## -remarks



<b>MAX_FILE_ASSOC_EXTENSION_SIZE</b> is declared as follows:

<code>#define MAX_FILE_ASSOC_EXTENSION_SIZE 256</code>




## -see-also




<a href="https://msdn.microsoft.com/BD4761C7-377C-499C-B984-3B126C704089">pluginResource2</a>
 

 

