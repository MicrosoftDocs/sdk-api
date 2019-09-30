---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetAssemblyFromScope
title: IMetaDataAssemblyImport::GetAssemblyFromScope (rometadataapi.h)
author: windows-sdk-content
description: Gets a pointer to the assembly in the current scope.
old-location: winrt\imetadataassemblyimport_getassemblyfromscope.htm
tech.root: WinRT
ms.assetid: b7b7d650-2db6-4e7c-92e0-5d0055a0a5a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAssemblyFromScope, GetAssemblyFromScope method [Windows Runtime], GetAssemblyFromScope method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetAssemblyFromScope method, IMetaDataAssemblyImport.GetAssemblyFromScope, IMetaDataAssemblyImport::GetAssemblyFromScope, rometadataapi/IMetaDataAssemblyImport::GetAssemblyFromScope, winrt.imetadataassemblyimport_getassemblyfromscope
ms.topic: method
f1_keywords: 
 - "rometadataapi/IMetaDataAssemblyImport.GetAssemblyFromScope"
req.header: rometadataapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataAssemblyImport.GetAssemblyFromScope
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>
 

 

