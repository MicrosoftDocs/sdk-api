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

# _SOURCE_MEDIA_A structure


## -description


The 
<b>SOURCE_MEDIA</b> structure is used with the 
<a href="https://msdn.microsoft.com/6a7947de-1bb3-46e0-9334-405684e58e98">SPFILENOTIFY_NEEDMEDIA</a> notification to pass source media information.


## -struct-fields




### -field Reserved

This member is not currently used.


### -field Tagfile

Optional  tag file that can be used to identify the source media.


### -field Description

Human-readable description of the source media.


### -field SourcePath

Path to the source that needs the new media.


### -field SourceFile

Source file to be retrieved from the new media.


### -field Flags

Copy style information that modifies how errors are handled. This member can be one or more of the following values. 







#### SP_COPY_WARNIFSKIP

Inform the user that skipping the file may affect the installation.



#### SP_COPY_NOSKIP

Do not offer the user the option to skip the file.



#### SP_FLAG_CABINETCONTINUATION

The current source file is continued in another cabinet file.



#### SP_COPY_NOBROWSE

Do not offer the user the option to browse.


## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/6a7947de-1bb3-46e0-9334-405684e58e98">SPFILENOTIFY_NEEDMEDIA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

