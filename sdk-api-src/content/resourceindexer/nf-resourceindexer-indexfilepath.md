---
UID: NF:resourceindexer.IndexFilePath
title: IndexFilePath function
author: windows-sdk-content
description: Indexes a file path for file and folder naming conventions.
old-location: menurc\indexfilepath.htm
old-project: menurc
ms.assetid: A1CDA9D1-9FEE-4FCB-AA85-1DA58D9EF95B
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IndexFilePath, IndexFilePath function [Menus and Other Resources], menurc.indexfilepath, resourceindexer/IndexFilePath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: resourceindexer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WitnessTagUpdateHelper
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mrmsupport.dll
api_name:
 - IndexFilePath
product: Windows
targetos: Windows
req.lib: Mrmsupport.lib
req.dll: Mrmsupport.dll
req.irql: 
req.product: ADAM
---

# IndexFilePath function


## -description


Indexes a file path for file and folder naming conventions.


## -parameters




### -param resourceIndexer [in]

The resource indexer object that you created by calling the <a href="https://msdn.microsoft.com/240C94B6-DF61-4C84-9047-9CD81A6FF4B4">CreateResourceIndexer</a> function.


### -param filePath [in]

The path for the folder that you want to index. The path must be an absolute path with the drive letter specified. Long file paths are not supported.


### -param ppResourceUri [out]

A uniform resource indicator (URI) that uses the ms-resource URI scheme and represents the named resource for the candidate, where the authority of the URI or the resource map is empty. For example, ms-resource:///Resources/String1 or ms-resource:///Files/images/logo.png.


### -param pQualifierCount [out]

The number of indexed resource qualifiers that the list in the <i>ppQualifiers</i> parameter contains.


### -param ppQualifiers [out]

A list of indexed resource qualifiers that declare the context under which the resources are appropriate.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/240C94B6-DF61-4C84-9047-9CD81A6FF4B4">CreateResourceIndexer</a>



<a href="https://msdn.microsoft.com/A6F253AD-0756-4996-AC6C-5B09C55DE22E">IndexedResourceQualifier</a>
 

 

