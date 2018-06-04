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

# _FILE_IN_CABINET_INFO_W structure


## -description


The 
<b>FILE_IN_CABINET_INFO</b> structure provides information about a file found in the cabinet. The 
<a href="https://msdn.microsoft.com/2fa2d140-fa8e-41a8-9800-d10e5559fab4">SetupIterateCabinet</a> function sends this structure as one of the parameters when it sends a 
<a href="https://msdn.microsoft.com/c6d89759-c0d4-4741-b992-43eaa0dc4f01">SPFILENOTIFY_FILEINCABINET</a> notification to the cabinet callback routine.


## -struct-fields




### -field NameInCabinet

File name as it exists within the cabinet file.


### -field FileSize

Uncompressed size of the file in the cabinet, in bytes.


### -field Win32Error

If an error occurs, this member is the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If no error has occurred, it is  NO_ERROR.


### -field DosDate

Date that the file was last saved.


### -field DosTime

MS-DOS time stamp of the file in the cabinet.


### -field DosAttribs

Attributes of the file in the cabinet.


### -field FullTargetName

Target path and file name.


## -see-also




<a href="https://msdn.microsoft.com/205bff19-d9ac-4dc0-ab11-92cf70a3bd49">CABINET_INFO</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

