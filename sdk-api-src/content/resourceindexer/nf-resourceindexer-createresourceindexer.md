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



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/42DCE463-B883-4564-9B7E-DEFF0A17CC1C">DestroyResourceIndexer</a>
 

 

