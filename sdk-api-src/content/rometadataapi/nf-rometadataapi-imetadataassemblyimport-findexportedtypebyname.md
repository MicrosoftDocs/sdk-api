---
UID: NF:rometadataapi.IMetaDataAssemblyImport.FindExportedTypeByName
title: IMetaDataAssemblyImport::FindExportedTypeByName
author: windows-sdk-content
description: Gets a pointer to an exported type, given its name and enclosing type.
old-location: winrt\imetadataassemblyimport_findexportedtypebyname.htm
old-project: WinRT
ms.assetid: 2b19b41c-fd1b-4284-8455-2b0d69907c99
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FindExportedTypeByName, FindExportedTypeByName method [Windows Runtime], FindExportedTypeByName method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],FindExportedTypeByName method, IMetaDataAssemblyImport.FindExportedTypeByName, IMetaDataAssemblyImport::FindExportedTypeByName, rometadataapi/IMetaDataAssemblyImport::FindExportedTypeByName, winrt.imetadataassemblyimport_findexportedtypebyname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IMetaDataAssemblyImport.FindExportedTypeByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataAssemblyImport::FindExportedTypeByName


## -description


Gets a pointer to an exported type, given its name and enclosing type.


## -parameters




### -param szName [in]

The name of the exported type.


### -param mdtExportedType [in]

The metadata token for the enclosing class of the exported type. This value is <b>mdExportedTypeNil</b> if the requested exported type is not a nested type.


### -param ptkExportedType [out]

A pointer to the <b>mdExportedType</b> token that represents the exported type.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method uses the standard rules employed by the common language runtime for resolving references.




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

