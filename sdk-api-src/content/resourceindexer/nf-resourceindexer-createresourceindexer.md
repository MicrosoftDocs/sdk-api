---
UID: NF:resourceindexer.CreateResourceIndexer
title: CreateResourceIndexer function (resourceindexer.h)
description: Creates a new resource indexer for the specified paths of the root of the project files and the extension DLL.
helpviewer_keywords: ["CreateResourceIndexer","CreateResourceIndexer function [Menus and Other Resources]","menurc.createresourceindexer","resourceindexer/CreateResourceIndexer"]
old-location: menurc\createresourceindexer.htm
tech.root: menurc
ms.assetid: 240C94B6-DF61-4C84-9047-9CD81A6FF4B4
ms.date: 12/05/2018
ms.keywords: CreateResourceIndexer, CreateResourceIndexer function [Menus and Other Resources], menurc.createresourceindexer, resourceindexer/CreateResourceIndexer
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
req.lib: Mrmsupport.lib
req.dll: Mrmsupport.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateResourceIndexer
 - resourceindexer/CreateResourceIndexer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mrmsupport.dll
api_name:
 - CreateResourceIndexer
---

# CreateResourceIndexer function


## -description

Creates a new resource indexer for the specified paths of the root of the project files and the extension DLL.

## -parameters

### -param projectRoot [in]

The path of the root folder to use for the project for the files to be produced, in string form. This path is used to determine file paths relative to the package that contains them. This path must be an absolute path with the drive letter specified. Long file paths are not supported.

### -param extensionDllPath [in, optional]

 The full path to an extension dynamic-link library (DLL) that is Microsoft-signed and implements the ext-ms-win-mrmcorer-environment-l1 API set. This path determines the file path from where the extension DLL for the modern resource technology (MRT) environment is loaded. This path must be an absolute path with the drive letter specified. Long file paths are not supported.

### -param ppResourceIndexer [out]

The newly created resource indexer.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/resourceindexer/nf-resourceindexer-destroyresourceindexer">DestroyResourceIndexer</a>