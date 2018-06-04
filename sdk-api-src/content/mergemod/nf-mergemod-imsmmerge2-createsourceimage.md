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

# IMsmMerge2::CreateSourceImage


## -description


The 
<b>CreateSourceImage</b> method enables the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration. For more information, see the 
<a href="https://msdn.microsoft.com/c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9">CreateSourceImage</a> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object.


## -parameters




### -param Path [in]

The path of the root of the source image for the install.


### -param fLongFileNames [in]

<i>fLongFileNames</i> determines whether or not long file names are used for both path segments and final file names.


### -param pFilePaths [out]

A pointer to a memory location. This memory location receives a second pointer to a string enumerator containing a list of fully qualified paths for the files that were extracted. The list is empty if no files can be extracted. This argument may be null. No list is provided if <i>pFilePaths</i> is Null.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

