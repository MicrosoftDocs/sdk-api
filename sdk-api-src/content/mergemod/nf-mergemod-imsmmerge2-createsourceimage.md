---
UID: NF:mergemod.IMsmMerge2.CreateSourceImage
title: IMsmMerge2::CreateSourceImage (mergemod.h)
author: windows-sdk-content
description: The CreateSourceImage method enables the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration.
old-location: setup\imsmmerge2_createsourceimage.htm
tech.root: Msi
ms.assetid: c42fa644-f0e6-4261-af76-741df572df3a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateSourceImage, CreateSourceImage method, CreateSourceImage method,IMsmMerge2 interface, IMsmMerge2 interface,CreateSourceImage method, IMsmMerge2.CreateSourceImage, IMsmMerge2::CreateSourceImage, _msi_createsourceimage_function, mergemod/IMsmMerge2::CreateSourceImage, setup.imsmmerge2_createsourceimage
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge2.CreateSourceImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmMerge2::CreateSourceImage


## -description


The 
<b>CreateSourceImage</b> method enables the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration. For more information, see the 
<a href="https://msdn.microsoft.com/c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9">CreateSourceImage</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object.


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
 

 

