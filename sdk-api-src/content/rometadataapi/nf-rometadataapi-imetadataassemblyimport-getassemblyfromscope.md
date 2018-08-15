---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetAssemblyFromScope
title: IMetaDataAssemblyImport::GetAssemblyFromScope
author: windows-sdk-content
description: Gets a pointer to the assembly in the current scope.
old-location: winrt\imetadataassemblyimport_getassemblyfromscope.htm
old-project: WinRT
ms.assetid: b7b7d650-2db6-4e7c-92e0-5d0055a0a5a9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetAssemblyFromScope, GetAssemblyFromScope method [Windows Runtime], GetAssemblyFromScope method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetAssemblyFromScope method, IMetaDataAssemblyImport.GetAssemblyFromScope, IMetaDataAssemblyImport::GetAssemblyFromScope, rometadataapi/IMetaDataAssemblyImport::GetAssemblyFromScope, winrt.imetadataassemblyimport_getassemblyfromscope
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rometadataapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataAssemblyImport.GetAssemblyFromScope
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataAssemblyImport::GetAssemblyFromScope


## -description


Gets a pointer to the assembly in the current scope.


## -parameters




### -param ptkAssembly [out]

A pointer to the retrieved <b>mdAssembly</b> token that identifies the assembly.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

