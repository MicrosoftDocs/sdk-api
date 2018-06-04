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

# PathMakeUniqueName function


## -description


Creates a unique path name from a template.


## -parameters




### -param pszUniqueName [out]

Type: <b>PWSTR</b>

A buffer that receives a null-terminated Unicode string that contains the unique path name. It should be at least MAX_PATH characters in length.


### -param cchMax

Type: <b>UINT</b>

The number of characters in the buffer pointed to by <i>pszUniqueName</i>.


### -param pszTemplate [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains a template that is used to construct the unique name. This template is used for drives that require file names with the 8.3 format. This string should be no more than MAX_PATH characters in length, including the terminating null character.


### -param pszLongPlate [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains a template that is used to construct the unique name. This template is used for drives that support long file names. This string should be no more than MAX_PATH characters in length, including the terminating null character.


### -param pszDir [in, optional]

Type: <b>PCWSTR</b>

A null-terminated string that contains the directory in which the new file resides. This string should be no more than MAX_PATH characters in length, including the terminating null character.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.




## -remarks



This function generates a new unique file name based on the templates specified by <i>pszTemplate</i>, for drives that require the 8.3 format, and <i>pszLongPlate</i> for drives that support long file names. For example, if you specify "My New Filename" for <i>pszLongPlate</i>, <b>PathMakeUniqueName</b> returns names such as "My New Filename (1)", "My New Filename (2)", and so on.



