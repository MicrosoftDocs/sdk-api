---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetManifestResourceProps
title: IMetaDataAssemblyImport::GetManifestResourceProps
author: windows-sdk-content
description: Gets the set of properties of the manifest resource with the specified metadata signature.
old-location: winrt\imetadataassemblyimport_getmanifestresourceprops.htm
tech.root: WinRT
ms.assetid: caa859c8-de40-4de6-bf90-41104cef91b2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetManifestResourceProps, GetManifestResourceProps method [Windows Runtime], GetManifestResourceProps method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetManifestResourceProps method, IMetaDataAssemblyImport.GetManifestResourceProps, IMetaDataAssemblyImport::GetManifestResourceProps, rometadataapi/IMetaDataAssemblyImport::GetManifestResourceProps, winrt.imetadataassemblyimport_getmanifestresourceprops
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMetaDataAssemblyImport.GetManifestResourceProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataAssemblyImport::GetManifestResourceProps


## -description


Gets the set of properties of the manifest resource with the specified metadata signature.


## -parameters




### -param mdmr [in]

An <b>mdManifestResource</b> token that represents the resource for which to get the properties.


### -param szName [out]

The name of the resource.


### -param cchName [in]

The size, in wide chars, of <i>szName</i>.


### -param pchName [out]

A pointer to the number of wide chars actually returned in <i>szName</i>.


### -param ptkImplementation [out]

A pointer to an <b>mdFile</b> token or an <b>mdAssemblyRef</b> token that represents the file or assembly, respectively, that contains the resource.


### -param pdwOffset [out]

A pointer to a value that specifies the offset to the beginning of the resource within the file.


### -param pdwResourceFlags [out]

A pointer to flags that describe the metadata applied to a resource. The flags value is a combination of one or more <a href="http://msdn.microsoft.com/en-us/library/ms230274.aspx">CorManifestResourceFlags</a> values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

