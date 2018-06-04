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

# WofEnumFilesProc callback function


## -description


Callback function that gets called for each file backed by an external data source, such as a WIM file.


## -parameters




### -param FilePath [in]

Specifies the path to the file which is backed by an external data source.


### -param ExternalFileInfo [in]

Points to a buffer containing information about the data source backing the file.  The type of this buffer depends on the provider; data structures for each provider are:

<table>
<tr>
<td>WOF_PROVIDER_WIM</td>
<td>WIM_EXTERNAL_FILE_INFO</td>
</tr>
<tr>
<td>WOF_PROVIDER_FILE</td>
<td>WOF_FILE_COMPRESSION_INFO</td>
</tr>
</table>
 


### -param UserData [in, optional]

Optional user defined data.


## -returns



A boolean value that indicates whether the enumeration was successful. The enumeration will stop if this callback function returns FALSE.



