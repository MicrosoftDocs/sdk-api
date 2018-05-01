---
UID: NF:resourceindexer.CreateResourceIndexer
title: CreateResourceIndexer function
author: windows-driver-content
description: Creates a new resource indexer for the specified paths of the root of the project files and the extension DLL.
old-location: menurc\createresourceindexer.htm
old-project: menurc
ms.assetid: 240C94B6-DF61-4C84-9047-9CD81A6FF4B4
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: CreateResourceIndexer, CreateResourceIndexer function [Menus and Other Resources], menurc.createresourceindexer, resourceindexer/CreateResourceIndexer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WitnessTagUpdateHelper
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mrmsupport.dll
api_name:
-	CreateResourceIndexer
product: Windows
targetos: Windows
req.lib: Mrmsupport.lib
req.dll: Mrmsupport.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

