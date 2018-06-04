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

# _FILE_RENAME_INFO structure


## -description


Contains the name to which the file should be renamed. Use only when calling 
   <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.ReplaceIfExists

<b>TRUE</b> to replace the file; otherwise, <b>FALSE</b>.


### -field DUMMYUNIONNAME.Flags

 


### -field ReplaceIfExists

<b>TRUE</b> to replace the file; otherwise, <b>FALSE</b>.


### -field RootDirectory

A handle to the root directory in which the file to be renamed is located.


### -field FileNameLength

The size of <b>FileName</b> in bytes.


### -field FileName

The new file name.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

