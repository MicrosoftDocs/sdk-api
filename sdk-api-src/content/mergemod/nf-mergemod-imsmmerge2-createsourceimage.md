---
UID: NF:mergemod.IMsmMerge2.CreateSourceImage
title: IMsmMerge2::CreateSourceImage (mergemod.h)
description: The CreateSourceImage method enables the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration.
helpviewer_keywords: ["CreateSourceImage","CreateSourceImage method","CreateSourceImage method","IMsmMerge2 interface","IMsmMerge2 interface","CreateSourceImage method","IMsmMerge2.CreateSourceImage","IMsmMerge2::CreateSourceImage","_msi_createsourceimage_function","mergemod/IMsmMerge2::CreateSourceImage","setup.imsmmerge2_createsourceimage"]
old-location: setup\imsmmerge2_createsourceimage.htm
tech.root: setup
ms.assetid: c42fa644-f0e6-4261-af76-741df572df3a
ms.date: 12/05/2018
ms.keywords: CreateSourceImage, CreateSourceImage method, CreateSourceImage method,IMsmMerge2 interface, IMsmMerge2 interface,CreateSourceImage method, IMsmMerge2.CreateSourceImage, IMsmMerge2::CreateSourceImage, _msi_createsourceimage_function, mergemod/IMsmMerge2::CreateSourceImage, setup.imsmmerge2_createsourceimage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmMerge2::CreateSourceImage
 - mergemod/IMsmMerge2::CreateSourceImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge2.CreateSourceImage
---

# IMsmMerge2::CreateSourceImage


## -description

The 
<b>CreateSourceImage</b> method enables the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration. For more information, see the 
<a href="/windows/desktop/Msi/merge-createsourceimage">CreateSourceImage</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object.

## -parameters

### -param Path [in]

The path of the root of the source image for the install.

### -param fLongFileNames [in]

<i>fLongFileNames</i> determines whether or not long file names are used for both path segments and final file names.

### -param pFilePaths [out]

A pointer to a memory location. This memory location receives a second pointer to a string enumerator containing a list of fully qualified paths for the files that were extracted. The list is empty if no files can be extracted. This argument may be null. No list is provided if <i>pFilePaths</i> is Null.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>