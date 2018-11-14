---
UID: NF:shobjidl_core.FreeKnownFolderDefinitionFields
title: FreeKnownFolderDefinitionFields function
author: windows-sdk-content
description: Frees the allocated fields in the result from IKnownFolder::GetFolderDefinition.
old-location: shell\FreeKnownFolderDefinitionFields.htm
tech.root: shell
ms.assetid: 0ad17dd3-e612-403a-b8c3-e93d5f259c1f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FreeKnownFolderDefinitionFields, FreeKnownFolderDefinitionFields function [Windows Shell], _shell_FreeKnownFolderDefinitionFields, shell.FreeKnownFolderDefinitionFields, shobjidl_core/FreeKnownFolderDefinitionFields
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - FreeKnownFolderDefinitionFields
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FreeKnownFolderDefinitionFields
: 
---

# FreeKnownFolderDefinitionFields function


## -description


Frees the allocated fields in the result from <a href="https://msdn.microsoft.com/b6f544cc-f487-405c-915d-b3a6dc59422c">IKnownFolder::GetFolderDefinition</a>.


## -parameters




### -param pKFD [in]

Type: <b><a href="https://msdn.microsoft.com/08bd8406-68fa-4e02-9a64-ed5e62f8639b">KNOWNFOLDER_DEFINITION</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/08bd8406-68fa-4e02-9a64-ed5e62f8639b">KNOWNFOLDER_DEFINITION</a> structure that contains information about the given known folder.


## -returns



This function does not return a value.




## -remarks



This is an inline helper function that calls <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> on the fields in the structure that need to be freed. Its implementation can be seen in the header file.




## -see-also




<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

